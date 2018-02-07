---
title: "さまざまな店舗からの注文を出荷します。"
description: "このトピックでは、請求金額の送信機能について説明します。"
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 7612935c42ee7b28e1d1e24b22801e31114dc675
ms.contentlocale: ja-jp
ms.lasthandoff: 02/07/2018

---

# <a name="ship-an-order-from-a-different-store"></a><span data-ttu-id="aefe0-103">さまざまな店舗からの注文を出荷します。</span><span class="sxs-lookup"><span data-stu-id="aefe0-103">Ship an order from a different store</span></span>

<span data-ttu-id="aefe0-104">Dynamics 365 for Retail の請求金額送信機能で、顧客注文を 1 つの店舗で受けて、別の店舗から出荷することができます。</span><span class="sxs-lookup"><span data-stu-id="aefe0-104">With the Charge send feature in Dynamics 365 for Retail, customer orders can be placed in one store and shipped from another store.</span></span> <span data-ttu-id="aefe0-105">小売販売時点管理 (POS) クライアントでの顧客注文は、複数の調達オプションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="aefe0-105">Customer orders in the point of sale (POS) client support multiple fulfillment options.</span></span> <span data-ttu-id="aefe0-106">調達のためのオプションの例を示します。</span><span class="sxs-lookup"><span data-stu-id="aefe0-106">Some examples of fulfillment options include:</span></span>
-   <span data-ttu-id="aefe0-107">別の日付に、同じ店舗から集荷します。</span><span class="sxs-lookup"><span data-stu-id="aefe0-107">Pick up from the same store on a different date.</span></span>
-   <span data-ttu-id="aefe0-108">同じ日付または異なる日付に、別の店から集荷します。</span><span class="sxs-lookup"><span data-stu-id="aefe0-108">Pick up from a different store on the same date or a different date.</span></span>
-   <span data-ttu-id="aefe0-109">その店舗に割り当てられている既定の出荷倉庫から出荷し、特定の日付に配送します。</span><span class="sxs-lookup"><span data-stu-id="aefe0-109">Ship from the default shipping warehouse that is assigned to the store, and deliver on a specific date.</span></span>

<span data-ttu-id="aefe0-110">請求金額送信機能は次の POS 操作を使用しています。すべての製品を出荷および選択した製品を出荷します。</span><span class="sxs-lookup"><span data-stu-id="aefe0-110">The Charge send feature uses the following POS operations: Ship all products and Ship selected products.</span></span> <span data-ttu-id="aefe0-111">これにより、店舗担当者は注文または注文明細行を充当する「出荷元」の場所を選択できます。</span><span class="sxs-lookup"><span data-stu-id="aefe0-111">This allows the store clerk to select the “ship from” location that the order or order line can be fulfilled from.</span></span> <span data-ttu-id="aefe0-112">既定では、「出荷元」の場所は、店舗に関連付けられている出荷倉庫です。</span><span class="sxs-lookup"><span data-stu-id="aefe0-112">By default, the “ship from” location is the shipping warehouse that is associated with the store.</span></span> <span data-ttu-id="aefe0-113">ただし、店舗担当者は、この場所を変更し、店舗に割り当てられた店舗ロケーター グループで定義されている店舗を選択することができます。</span><span class="sxs-lookup"><span data-stu-id="aefe0-113">However, the store clerk can change this location and select any store that is defined in the store locator group that is assigned to the store.</span></span> 

<span data-ttu-id="aefe0-114">「出荷先」アドレスを選択する機能は変わりません。</span><span class="sxs-lookup"><span data-stu-id="aefe0-114">The ability to select “ship to” addresses remains unchanged.</span></span> 

<span data-ttu-id="aefe0-115">注文明細行を処理するために使用できる出荷方法は、製品と住所の有効な荷渡方法の設定に基づいています。</span><span class="sxs-lookup"><span data-stu-id="aefe0-115">The shipping methods that can be used to fulfill the order line are based on the configuration of valid modes of delivery for products and addresses.</span></span> <span data-ttu-id="aefe0-116">荷渡方法の有効性に関するルールは、小売用バック オフィス (HQ) でのみ維持されるため、POS クライアントは出荷明細行の有効な荷渡方法を取得するためにリアルタイムの呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="aefe0-116">Because the rules about valid of modes of delivery are maintained only in the Retail headquarters (HQ), the POS client makes a real-time call to fetch the valid modes of delivery for a ship line.</span></span> 


