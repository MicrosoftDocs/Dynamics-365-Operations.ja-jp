---
title: 買い物カゴ アイコン モジュール
description: このトピックでは、買い物カゴ アイコン モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: 8cc96e0476a9d8a46aed7011359dc65fbc678fbf
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261576"
---
# <a name="cart-icon-module"></a><span data-ttu-id="5cc86-103">買い物カゴ アイコン モジュール</span><span class="sxs-lookup"><span data-stu-id="5cc86-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5cc86-104">このトピックでは、買い物カゴ アイコン モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5cc86-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5cc86-105">概要</span><span class="sxs-lookup"><span data-stu-id="5cc86-105">Overview</span></span>

<span data-ttu-id="5cc86-106">買い物カゴ アイコン モジュールは、ページのヘッダー モジュールで買い物カゴを表し、買い物カゴ内の品目数を示します。</span><span class="sxs-lookup"><span data-stu-id="5cc86-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="5cc86-107">買い物カゴ アイコン モジュールには、買い物カゴ アイコンにカーソルを合わせると、買い物カゴの概要 (ミニカートとも呼ばれる) も表示されます。</span><span class="sxs-lookup"><span data-stu-id="5cc86-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="5cc86-108">ミニ カートには、買い物カゴ ページに移動することなく、買い物カゴ内の品目の概要が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5cc86-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="5cc86-109">また、ユーザーが概要に満足している場合、チェックアウト ページに直接移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="5cc86-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="5cc86-110">これにより、ページ ナビゲーションの回数が減り、迅速にチェックアウトできるようになります。</span><span class="sxs-lookup"><span data-stu-id="5cc86-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="5cc86-111">モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="5cc86-111">Module properties</span></span>

- <span data-ttu-id="5cc86-112">**ミニ カートの表示** – True の場合、このプロパティにより、買い物カゴ アイコンにカーソルを合わせると買い物カゴの概要 (ミニ カート) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5cc86-112">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="5cc86-113">この機能は、デスクトップ 表示ポートに対してのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="5cc86-113">This functionality is only supported for desktop view ports.</span></span>


## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="5cc86-114">買い物カゴ アイコン モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="5cc86-114">Add a cart icon module to a page</span></span>

<span data-ttu-id="5cc86-115">買い物カゴ アイコン モジュールを追加するには、[ヘッダー モジュール](author-header-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5cc86-115">To add a cart icon module, see [Header module](author-header-module.md).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="5cc86-116">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5cc86-116">Additional resources</span></span>

[<span data-ttu-id="5cc86-117">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="5cc86-117">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="5cc86-118">買い物カゴ モジュール</span><span class="sxs-lookup"><span data-stu-id="5cc86-118">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="5cc86-119">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="5cc86-119">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="5cc86-120">注文確認モジュール</span><span class="sxs-lookup"><span data-stu-id="5cc86-120">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="5cc86-121">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="5cc86-121">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="5cc86-122">フッター モジュール</span><span class="sxs-lookup"><span data-stu-id="5cc86-122">Footer module</span></span>](author-footer-module.md)
