---
title: 注文詳細のモジュール
description: このトピックでは、注文詳細モジュールおよび Microsoft Dynamics 365 Commerce での使用方法について説明します。
author: anupamar
manager: annbe
ms.date: 06/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5876b953a3b3d960c106acf37731fde13b93f8e7
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661175"
---
# <a name="order-details-module"></a><span data-ttu-id="87ad6-103">注文詳細のモジュール</span><span class="sxs-lookup"><span data-stu-id="87ad6-103">Order details module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="87ad6-104">このトピックでは、注文詳細モジュールおよび Microsoft Dynamics 365 Commerce での使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="87ad6-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="87ad6-105">概要</span><span class="sxs-lookup"><span data-stu-id="87ad6-105">Overview</span></span>

<span data-ttu-id="87ad6-106">注文詳細モジュールを使用して、注文が行われた後、注文確認の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="87ad6-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="87ad6-107">注文の確認 ID、注文の連絡先情報、およびその他の注文の詳細 (購入された品目、支払情報、出荷方法など) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="87ad6-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-details-module-properties"></a><span data-ttu-id="87ad6-108">注文詳細モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="87ad6-108">Order details module properties</span></span>

| <span data-ttu-id="87ad6-109">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="87ad6-109">Property name</span></span>  | <span data-ttu-id="87ad6-110">値</span><span class="sxs-lookup"><span data-stu-id="87ad6-110">Values</span></span> | <span data-ttu-id="87ad6-111">説明</span><span class="sxs-lookup"><span data-stu-id="87ad6-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="87ad6-112">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="87ad6-112">Heading</span></span>        | <span data-ttu-id="87ad6-113">ヘッダー テキストとヘッダー タグ (**H1**、**H2**、**H3**、**H4**、**H5**、または **H6**)</span><span class="sxs-lookup"><span data-stu-id="87ad6-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="87ad6-114">注文詳細モジュールには、ヘッダーを付けることができます。</span><span class="sxs-lookup"><span data-stu-id="87ad6-114">The order details module can have a heading.</span></span> <span data-ttu-id="87ad6-115">既定では、**H2** ヘッダー タグがヘッダーに使用されます。</span><span class="sxs-lookup"><span data-stu-id="87ad6-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="87ad6-116">ただし、アクセシビリティ要件を満たすようにタグを変更できます。</span><span class="sxs-lookup"><span data-stu-id="87ad6-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="87ad6-117">連絡先番号</span><span class="sxs-lookup"><span data-stu-id="87ad6-117">Contact number</span></span> | <span data-ttu-id="87ad6-118">テキスト</span><span class="sxs-lookup"><span data-stu-id="87ad6-118">Text</span></span> | <span data-ttu-id="87ad6-119">連絡先番号は、注文に関連する質問に対して発行できます。</span><span class="sxs-lookup"><span data-stu-id="87ad6-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="87ad6-120">注文詳細ページで使用可能なモジュール</span><span class="sxs-lookup"><span data-stu-id="87ad6-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="87ad6-121">注文の詳細ページを作成するときに、注文明細モジュールに加えて、他の関連モジュールを追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="87ad6-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="87ad6-122">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="87ad6-122">Here are some examples:</span></span>

- <span data-ttu-id="87ad6-123">**推奨モジュール** - 推奨モジュールを注文詳細ページに追加して、顧客に他の製品を提案することができます。</span><span class="sxs-lookup"><span data-stu-id="87ad6-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="87ad6-124">**マーケティング モジュール** - 注文詳細ページにマーケティング モジュールを追加して、マーケティング コンテンツを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="87ad6-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="add-an-order-details-module-to-a-page"></a><span data-ttu-id="87ad6-125">注文詳細モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="87ad6-125">Add an order details module to a page</span></span>

<span data-ttu-id="87ad6-126">新規ページに注文詳細モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="87ad6-126">To add an order details module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="87ad6-127">**テンプレート** に移動し、**新規** を選択して新たなテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="87ad6-127">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="87ad6-128">**テンプレート名** 下の **新規テンプレート** ダイアログ ボックスに、**注文詳細テンプレート** の名称を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87ad6-128">In the **New Template** dialog box, under **Template name**, enter the name **Order details template**, and then select **OK**.</span></span>
1. <span data-ttu-id="87ad6-129">**本文** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87ad6-129">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="87ad6-130">**モジュールの追加** ダイアログ ボックスで、**規定のページ** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87ad6-130">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="87ad6-131">**既定のページ**モジュールの**メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="87ad6-131">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="87ad6-132">**モジュールの追加** ダイアログ ボックスで、**注文の詳細** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87ad6-132">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="87ad6-133">**保存** を選択し、続いて **プレビュー** を選択してテンプレートをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="87ad6-133">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="87ad6-134">注文確認番号のコンテキストを必要とするため、注文詳細モジュールは表示されません。</span><span class="sxs-lookup"><span data-stu-id="87ad6-134">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="87ad6-135">**編集の完了**  を選択してテンプレートをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="87ad6-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="87ad6-136">**ページ** に移動し、**新規** を選択して新たなページを作成します。</span><span class="sxs-lookup"><span data-stu-id="87ad6-136">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="87ad6-137">**テンプレートの選択** ダイアログ ボックスで、**注文詳細テンプレート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87ad6-137">In the **Choose a template** dialog box, select **Order details template**.</span></span> <span data-ttu-id="87ad6-138">**ページ名** で、**注文詳細のページ** を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87ad6-138">Under **Page name**, enter **Order details page**, and then select **OK**.</span></span>
1. <span data-ttu-id="87ad6-139">**既定のページ**モジュールの**メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="87ad6-139">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="87ad6-140">**モジュールの追加** ダイアログ ボックスで、**注文の詳細** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87ad6-140">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="87ad6-141">注文詳細モジュールのプロパティ ウィンドウで、鉛筆の記号の横にある **見出し** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87ad6-141">In the properties pane for the order details module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="87ad6-142">**ヘッダー** ダイアログの **ヘッダー テキスト** フィールドで、ヘッダーテキストの **注文の詳細** を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87ad6-142">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order details**, and then select **OK**.</span></span>
1. <span data-ttu-id="87ad6-143">**保存** を選択し、 続いて**プレビュー** を選択してページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="87ad6-143">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="87ad6-144">**編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="87ad6-144">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="87ad6-145">追加リソース</span><span class="sxs-lookup"><span data-stu-id="87ad6-145">Additional resources</span></span>

[<span data-ttu-id="87ad6-146">買い物カゴ モジュール</span><span class="sxs-lookup"><span data-stu-id="87ad6-146">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="87ad6-147">買い物カゴ アイコン モジュール</span><span class="sxs-lookup"><span data-stu-id="87ad6-147">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="87ad6-148">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="87ad6-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="87ad6-149">支払モジュール</span><span class="sxs-lookup"><span data-stu-id="87ad6-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="87ad6-150">配送先住所モジュール</span><span class="sxs-lookup"><span data-stu-id="87ad6-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="87ad6-151">配送オプション モジュール</span><span class="sxs-lookup"><span data-stu-id="87ad6-151">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="87ad6-152">ギフト カード モジュール</span><span class="sxs-lookup"><span data-stu-id="87ad6-152">Gift card module</span></span>](add-giftcard.md)
