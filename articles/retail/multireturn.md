---
title: 複数の顧客注文および請求書間での品目の返品
description: このトピックでは、複数の顧客注文および請求書をまたいだ返品を有効にする Dynamics 365 Retail の機能について説明します。
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
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
ms.openlocfilehash: 25a1081e5f903076e23089c41dda7437f8a70124
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017992"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="3054d-103">複数の顧客注文および請求書間での品目の返品</span><span class="sxs-lookup"><span data-stu-id="3054d-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="3054d-104">複数の顧客注文および請求書間で返品が可能です。</span><span class="sxs-lookup"><span data-stu-id="3054d-104">Returns can be made across multiple orders and invoices.</span></span> 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="3054d-105">複数の顧客注文および請求書をまたいだ返品をサポートするように Retail を構成する</span><span class="sxs-lookup"><span data-stu-id="3054d-105">Configure Retail to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="3054d-106">**小売パラメーター \> 顧客注文**に移動します。</span><span class="sxs-lookup"><span data-stu-id="3054d-106">Go to **Retail parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="3054d-107">**複数の注文の返品を有効化**パラメーターをオンにします。</span><span class="sxs-lookup"><span data-stu-id="3054d-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="3054d-108">返品の処理</span><span class="sxs-lookup"><span data-stu-id="3054d-108">Process returns</span></span>

<span data-ttu-id="3054d-109">パラメーターをオンにし、変更を店舗に同期させると、店舗のレジ担当者は、顧客の返品に対して複数の販売注文を選択できるようになります。</span><span class="sxs-lookup"><span data-stu-id="3054d-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="3054d-110">注文を選択すると、その注文のすべての請求書で返品可能なすべての商品の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3054d-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="3054d-111">レジ担当者は、その一覧から返品する商品を選択できます。</span><span class="sxs-lookup"><span data-stu-id="3054d-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="3054d-112">選択したすべての商品に対して 1 つの返品注文が作成されます。</span><span class="sxs-lookup"><span data-stu-id="3054d-112">A single return order will be created for all the selected products.</span></span>
