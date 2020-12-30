---
title: 買い物カゴ アイコン モジュール
description: このトピックでは、買い物カゴ アイコン モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ebc5cfa490a4c8538fd081aced0844ed01d63a26
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2020
ms.locfileid: "4413912"
---
# <a name="cart-icon-module"></a><span data-ttu-id="fd536-103">買い物カゴ アイコン モジュール</span><span class="sxs-lookup"><span data-stu-id="fd536-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fd536-104">このトピックでは、買い物カゴ アイコン モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fd536-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fd536-105">概要</span><span class="sxs-lookup"><span data-stu-id="fd536-105">Overview</span></span>

<span data-ttu-id="fd536-106">買い物カゴ アイコン モジュールは、ページのヘッダー モジュールで買い物カゴを表し、買い物カゴ内の品目数を示します。</span><span class="sxs-lookup"><span data-stu-id="fd536-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="fd536-107">買い物カゴ アイコン モジュールには、買い物カゴ アイコンにカーソルを合わせると、買い物カゴの概要 (ミニカートとも呼ばれる) も表示されます。</span><span class="sxs-lookup"><span data-stu-id="fd536-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="fd536-108">ミニ カートには、買い物カゴ ページに移動することなく、買い物カゴ内の品目の概要が表示されます。</span><span class="sxs-lookup"><span data-stu-id="fd536-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="fd536-109">また、ユーザーが概要に満足している場合、チェックアウト ページに直接移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="fd536-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="fd536-110">これにより、ページ ナビゲーションの回数が減り、迅速にチェックアウトできるようになります。</span><span class="sxs-lookup"><span data-stu-id="fd536-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="fd536-111">Dynamics 365 Commerce 10.0.11 リリースは、買い物カゴ アイコン モジュールをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="fd536-111">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="fd536-112">次の図は、Fabrikam のヘッダーでミニ買い物カゴを表示する買い物カゴのアイコン モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="fd536-112">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![買い物カゴ アイコン モジュールの例](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="fd536-114">モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="fd536-114">Module properties</span></span>

- <span data-ttu-id="fd536-115">**ミニ カートの表示** – True の場合、このプロパティにより、買い物カゴ アイコンにカーソルを合わせると買い物カゴの概要 (ミニ カート) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="fd536-115">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="fd536-116">この機能は、デスクトップ 表示ポートに対してのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="fd536-116">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="fd536-117">買い物カゴ アイコン モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="fd536-117">Add a cart icon module to a page</span></span>

<span data-ttu-id="fd536-118">買い物カゴ アイコン モジュールを追加するには、[ヘッダー モジュール](author-header-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fd536-118">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fd536-119">追加リソース</span><span class="sxs-lookup"><span data-stu-id="fd536-119">Additional resources</span></span>

[<span data-ttu-id="fd536-120">買い物カゴ モジュール</span><span class="sxs-lookup"><span data-stu-id="fd536-120">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="fd536-121">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="fd536-121">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="fd536-122">支払モジュール</span><span class="sxs-lookup"><span data-stu-id="fd536-122">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="fd536-123">出荷先住所モジュール</span><span class="sxs-lookup"><span data-stu-id="fd536-123">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="fd536-124">配送オプション モジュール</span><span class="sxs-lookup"><span data-stu-id="fd536-124">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="fd536-125">集荷情報モジュール</span><span class="sxs-lookup"><span data-stu-id="fd536-125">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="fd536-126">注文詳細のモジュール</span><span class="sxs-lookup"><span data-stu-id="fd536-126">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="fd536-127">ギフト カード モジュール</span><span class="sxs-lookup"><span data-stu-id="fd536-127">Gift card module</span></span>](add-giftcard.md)
