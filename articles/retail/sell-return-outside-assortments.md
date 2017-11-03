---
title: "品揃えの範囲外の製品の販売と返品"
description: "Dynamics 365 for Retail で、品揃えの範囲外の製品を販売および返品ができます。"
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: fd00da1242964dddda5c19d46e61da33997e6d02
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="sell-and-return-products-outside-of-an-assortment"></a><span data-ttu-id="9417d-103">品揃えの範囲外の製品の販売と返品</span><span class="sxs-lookup"><span data-stu-id="9417d-103">Sell and return products outside of an assortment</span></span>
<span data-ttu-id="9417d-104">小売業者の一般的なシナリオでは、店舗で特定の製品を抱えていない場合 (つまり、製品が店舗の品揃えにない場合) でも、製品を顧客に販売したり、顧客からの返品を受け入れたりします。</span><span class="sxs-lookup"><span data-stu-id="9417d-104">A common scenario for any retailer is to sell products to their customers or accept returns from their customers even if they don’t carry the specific products in their store (in other words, the products are not assorted to the store).</span></span>
<span data-ttu-id="9417d-105">以下に一般的なシナリオを挙げます。</span><span class="sxs-lookup"><span data-stu-id="9417d-105">Here are some typical scenarios:</span></span>

+ <span data-ttu-id="9417d-106">小売業者は、特定の店舗ですべての製品を抱えているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="9417d-106">A retailer doesn’t carry all its products in a specific store.</span></span> <span data-ttu-id="9417d-107">残りの製品は、倉庫に格納されます。</span><span class="sxs-lookup"><span data-stu-id="9417d-107">The remaining products are stored in the warehouse.</span></span> <span data-ttu-id="9417d-108">店舗スタッフは、倉庫の製品を検索または表示することで顧客を支援し、カートに追加して、倉庫から住所へ出荷したり、現在の店舗または別の店舗から製品を顧客にピッキングしてもらったりなどの配送方法を選択することにより、チェックアウトを完了できます。</span><span class="sxs-lookup"><span data-stu-id="9417d-108">The store associate can assist the customer by searching or browsing for the products in the warehouse, add them to the cart, and complete the checkout by selecting a delivery method, such as shipping to an address from the warehouse or letting the customer pick up the product from the current store or from another store.</span></span>
+ <span data-ttu-id="9417d-109">小売業者は、店舗内に特定の製品を抱えたり、顧客が訪れた店舗に在庫を持ったりしませんが、製品を他の店舗で使用できます。</span><span class="sxs-lookup"><span data-stu-id="9417d-109">A retailer doesn’t carry specific products in the store or doesn’t have them in stock at the store the customer visited, but the products are available in other stores.</span></span> <span data-ttu-id="9417d-110">店舗スタッフは、その他の店舗の製品を検索または表示することで顧客を支援し、カートに追加して、配送方法を選択することにより、チェック アウトを完了できます。</span><span class="sxs-lookup"><span data-stu-id="9417d-110">The store associate can assist the customer by searching or browsing the products in the other store, add them to the cart, and complete the checkout by selecting a delivery method.</span></span>
+ <span data-ttu-id="9417d-111">小売業者が特定の市町村または郵便番号コードで多数の店舗を所有していれば、購入した同じ店舗への製品の返品を顧客に強制したくはありません。</span><span class="sxs-lookup"><span data-stu-id="9417d-111">A retailer has many stores in and around a specific city or zip code and doesn’t want to force the customers to return products to the same store they were purchased in.</span></span> <span data-ttu-id="9417d-112">代わりに、顧客は、どの店舗にも製品を返品することができます。</span><span class="sxs-lookup"><span data-stu-id="9417d-112">Instead, customers can return products to any store.</span></span>


<span data-ttu-id="9417d-113">これらの一般的なシナリオは、Dynamics 365 for Retail を使用している小売業者が使用できます。</span><span class="sxs-lookup"><span data-stu-id="9417d-113">Those common scenarios are available for retailers using Dynamics 365 for Retail.</span></span> <span data-ttu-id="9417d-114">Retail では次のことができます。</span><span class="sxs-lookup"><span data-stu-id="9417d-114">With Retail, you can:</span></span>
+ <span data-ttu-id="9417d-115">他の店舗で製品を検索や表示します。</span><span class="sxs-lookup"><span data-stu-id="9417d-115">Search or browse products at other stores.</span></span>
+ <span data-ttu-id="9417d-116">すべてリリースされた製品を検索や表示します。</span><span class="sxs-lookup"><span data-stu-id="9417d-116">Search or browse all released products.</span></span>
+ <span data-ttu-id="9417d-117">現金店頭払いのトランザクションまたは顧客注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="9417d-117">Create cash-and-carry transactions or customer orders.</span></span>
+ <span data-ttu-id="9417d-118">顧客注文の配送オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="9417d-118">Select delivery options for customer orders.</span></span>
+ <span data-ttu-id="9417d-119">現在の店舗または別の店舗で製品をピッキングします。</span><span class="sxs-lookup"><span data-stu-id="9417d-119">Pick up products at the current store or another store.</span></span>
+ <span data-ttu-id="9417d-120">現在の店舗または別の店舗で注文をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="9417d-120">Cancel an order at the current store or another store.</span></span>
+ <span data-ttu-id="9417d-121">現在の店舗または別の店舗に領収書の有無にかかわらず注文を返品します。</span><span class="sxs-lookup"><span data-stu-id="9417d-121">Return an order with or without the receipt at the current store or another store.</span></span>

