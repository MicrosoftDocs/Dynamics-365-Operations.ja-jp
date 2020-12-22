---
title: 複数の顧客注文および請求書間での品目の返品
description: このトピックでは、複数の顧客注文および請求書をまたいだ返品を有効にする Dynamics 365 Commerce の機能について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: e95f06ffaaf2d250b02a8458faa2d9e0b5ef5631
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4459380"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="6abb1-103">複数の顧客注文および請求書間での品目の返品</span><span class="sxs-lookup"><span data-stu-id="6abb1-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="6abb1-104">この記事では、複数の請求書に対して顧客の注文返品を最適化する 2 つの機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="6abb1-104">This article describes two features that optimize customer order returns over multiple invoices.</span></span> 

## <a name="enable-refunds-over-multiple-captures"></a><span data-ttu-id="6abb1-105">複数のキャプチャの払戻を有効にする</span><span class="sxs-lookup"><span data-stu-id="6abb1-105">Enable refunds over multiple captures</span></span>

<span data-ttu-id="6abb1-106">この機能は、同じ顧客注文に対してリンクされた複数の払戻を有効にします。</span><span class="sxs-lookup"><span data-stu-id="6abb1-106">This feature enables multiple linked refunds against the same customer order.</span></span> 

1. <span data-ttu-id="6abb1-107">**機能管理** ワークスペースに移動して、**複数のキャプチャの払戻を有効にする** を検索します。</span><span class="sxs-lookup"><span data-stu-id="6abb1-107">Go to the **Feature management** workspace and search for **Enable refunds over multiple captures**.</span></span>
2. <span data-ttu-id="6abb1-108">**複数の注文の払戻を有効にする** を選択して、**有効にする** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6abb1-108">Select **Enable refunds over multiple orders** and then click **Enable**.</span></span> 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a><span data-ttu-id="6abb1-109">一部の数量を使用して、返品の適切な税計算を有効にします</span><span class="sxs-lookup"><span data-stu-id="6abb1-109">Enable proper tax calculation for returns with partial quantity</span></span>

<span data-ttu-id="6abb1-110">この機能により、複数の請求書を使用して注文が返品された場合、最終的に税金は最初に請求された税額と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="6abb1-110">This feature ensures that when an order is returned using multiple invoices, the taxes will ultimately be equal to the tax amount originally charged.</span></span> 

1. <span data-ttu-id="6abb1-111">**機能管理** ワークスペースに移動して、**Enable proper tax calculation for returns with partial quantity (一部の数量を使用して、返品の適切な税計算を有効にする)** を検索します。</span><span class="sxs-lookup"><span data-stu-id="6abb1-111">Go to the **Feature management** workspace and search for **Enable proper tax calculation for returns with partial quantity**.</span></span>
2. <span data-ttu-id="6abb1-112">**Enable proper tax calculation for returns with partial quantity (一部の数量を使用して、返品の適切な税計算を有効にする)**、**有効にする** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6abb1-112">Select **Enable proper tax calculation for returns with partial quantity** and then click **Enable**.</span></span> 


## <a name="process-returns"></a><span data-ttu-id="6abb1-113">返品の処理</span><span class="sxs-lookup"><span data-stu-id="6abb1-113">Process returns</span></span>

<span data-ttu-id="6abb1-114">これらの機能をオンにし、変更を店舗に同期させると、店舗のレジ担当者は、顧客の返品に対して複数の販売注文を選択できるようになります。</span><span class="sxs-lookup"><span data-stu-id="6abb1-114">After these features are turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="6abb1-115">注文を選択すると、その注文のすべての請求書で返品可能なすべての製品の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6abb1-115">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="6abb1-116">レジ担当者は、その一覧から返品する商品を選択できます。</span><span class="sxs-lookup"><span data-stu-id="6abb1-116">The cashier can then select the products to return.</span></span> <span data-ttu-id="6abb1-117">選択したすべての製品に対して 1 つの返品注文が作成されます。</span><span class="sxs-lookup"><span data-stu-id="6abb1-117">A single return order will be created for all the selected products.</span></span>

<span data-ttu-id="6abb1-118">注文が完全に返品された場合、顧客に返金される税額は、最初に請求された税額と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="6abb1-118">If the order is fully returned, the amount of taxes returned to the customer will be equal to the amount of tax originally charged.</span></span>

