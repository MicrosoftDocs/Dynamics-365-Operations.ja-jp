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
ms.openlocfilehash: 9d916d2687777403f2b0df7c35171948ad2fb7db
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972749"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="be874-103">注文確認モジュール</span><span class="sxs-lookup"><span data-stu-id="be874-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="be874-104">このトピックでは、注文確認モジュールおよび Microsoft Dynamics 365 Commerce での使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="be874-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="be874-105">概要</span><span class="sxs-lookup"><span data-stu-id="be874-105">Overview</span></span>

<span data-ttu-id="be874-106">注文確認モジュールを使用して、注文が行われた後、注文確認の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="be874-106">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="be874-107">注文の確認 ID、注文の連絡先情報、およびその他の注文の詳細 (購入された品目、支払情報、集荷オプション、出荷方法など) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="be874-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="be874-108">注文確認モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="be874-108">Order confirmation module properties</span></span>

| <span data-ttu-id="be874-109">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="be874-109">Property name</span></span>  | <span data-ttu-id="be874-110">値</span><span class="sxs-lookup"><span data-stu-id="be874-110">Values</span></span> | <span data-ttu-id="be874-111">説明</span><span class="sxs-lookup"><span data-stu-id="be874-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="be874-112">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="be874-112">Heading</span></span>        | <span data-ttu-id="be874-113">ヘッダー テキストとヘッダー タグ (**H1**、**H2**、**H3**、**H4**、**H5**、または **H6**)</span><span class="sxs-lookup"><span data-stu-id="be874-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="be874-114">注文確認モジュールには、ヘッダーを付けることができます。</span><span class="sxs-lookup"><span data-stu-id="be874-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="be874-115">既定では、**H2** ヘッダー タグがヘッダーに使用されます。</span><span class="sxs-lookup"><span data-stu-id="be874-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="be874-116">ただし、アクセシビリティ要件を満たすようにタグを変更できます。</span><span class="sxs-lookup"><span data-stu-id="be874-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="be874-117">連絡先番号</span><span class="sxs-lookup"><span data-stu-id="be874-117">Contact number</span></span> | <span data-ttu-id="be874-118">テキスト</span><span class="sxs-lookup"><span data-stu-id="be874-118">Text</span></span> | <span data-ttu-id="be874-119">連絡先番号は、注文に関連する質問に対して発行できます。</span><span class="sxs-lookup"><span data-stu-id="be874-119">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="be874-120">集荷時間帯情報の表示</span><span class="sxs-lookup"><span data-stu-id="be874-120">Show pickup timeslot information</span></span> | <span data-ttu-id="be874-121">True または False</span><span class="sxs-lookup"><span data-stu-id="be874-121">True or False</span></span> | <span data-ttu-id="be874-122">このプロパティは Dynamics 365 Commerce、10.0.15 以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="be874-122">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="be874-123">True の場合は、集荷品目に対して集荷の時間帯情報が表示されます</span><span class="sxs-lookup"><span data-stu-id="be874-123">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="be874-124">注文確認ページで使用可能なモジュール</span><span class="sxs-lookup"><span data-stu-id="be874-124">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="be874-125">注文確認ページを作成するときに、注文確認モジュールに加えて、他の関連モジュールを追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="be874-125">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="be874-126">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="be874-126">Here are some examples:</span></span>

- <span data-ttu-id="be874-127">**推奨モジュール** – 推奨モジュールを注文確認ページに追加して、顧客に他の製品を提案することができます。</span><span class="sxs-lookup"><span data-stu-id="be874-127">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="be874-128">**マーケティング モジュール** - 注文確認ページにマーケティング モジュールを追加して、マーケティング コンテンツを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="be874-128">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="be874-129">注文確認モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="be874-129">Add an order confirmation module to a page</span></span>

<span data-ttu-id="be874-130">新規ページに注文確認モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="be874-130">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="be874-131">**テンプレート** に移動し、**新規** を選択して新たなテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="be874-131">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="be874-132">**テンプレート名** 下の **新規テンプレート** ダイアログ ボックスに、**注文確認テンプレート** の名称を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="be874-132">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="be874-133">**本文** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="be874-133">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="be874-134">**モジュールの追加** ダイアログ ボックスで、**規定のページ** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="be874-134">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="be874-135">**既定のページ** モジュールの **メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="be874-135">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="be874-136">**モジュールの追加** ダイアログ ボックスで、**注文の確認** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="be874-136">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="be874-137">**保存** を選択し、続いて **プレビュー** を選択してテンプレートをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="be874-137">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="be874-138">注文確認番号のコンテキストを必要とするため、注文確認モジュールは表示されないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="be874-138">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="be874-139">**編集の完了**  を選択してテンプレートをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="be874-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="be874-140">**ページ** に移動し、**新規** を選択して新たなページを作成します。</span><span class="sxs-lookup"><span data-stu-id="be874-140">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="be874-141">**テンプレートの選択** ダイアログ ボックスで、**注文確認テンプレート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="be874-141">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="be874-142">**ページ名** で、**注文確認のページ** を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="be874-142">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="be874-143">**既定のページ** モジュールの **メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="be874-143">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="be874-144">**モジュールの追加** ダイアログ ボックスで、**注文の確認** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="be874-144">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="be874-145">注文確認モジュールのプロパティ ウィンドウで、鉛筆の記号の横にある **見出し** を選択します。</span><span class="sxs-lookup"><span data-stu-id="be874-145">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="be874-146">**ヘッダー** ダイアログの **ヘッダー テキスト** フィールドで、ヘッダーテキストの **注文の確認** を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="be874-146">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="be874-147">**保存** を選択し、 続いて **プレビュー** を選択してページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="be874-147">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="be874-148">**編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="be874-148">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="be874-149">追加リソース</span><span class="sxs-lookup"><span data-stu-id="be874-149">Additional resources</span></span>

[<span data-ttu-id="be874-150">買い物カゴ モジュール</span><span class="sxs-lookup"><span data-stu-id="be874-150">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="be874-151">買い物カゴ アイコン モジュール</span><span class="sxs-lookup"><span data-stu-id="be874-151">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="be874-152">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="be874-152">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="be874-153">支払モジュール</span><span class="sxs-lookup"><span data-stu-id="be874-153">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="be874-154">出荷先住所モジュール</span><span class="sxs-lookup"><span data-stu-id="be874-154">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="be874-155">配送オプション モジュール</span><span class="sxs-lookup"><span data-stu-id="be874-155">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="be874-156">集荷情報モジュール</span><span class="sxs-lookup"><span data-stu-id="be874-156">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="be874-157">ギフト カード モジュール</span><span class="sxs-lookup"><span data-stu-id="be874-157">Gift card module</span></span>](add-giftcard.md)
