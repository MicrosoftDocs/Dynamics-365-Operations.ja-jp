---
title: 価格調整および割引
description: この記事は、Dynamics 365 Commerce における価格調整および割引についての情報を提供します。
author: scott-tucker
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 2d3e8025c5ab28296713634094694156f9addf62
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802794"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="5c4a6-103">価格調整および割引</span><span class="sxs-lookup"><span data-stu-id="5c4a6-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5c4a6-104">この記事は、Dynamics 365 Commerce における価格調整および割引についての情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="5c4a6-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5c4a6-105">コマースでは、製品の価格を調整したり、POS、コール センターの販売注文、またはオンライン注文で明細行品目またはトランザクションに適用される割引を設定したりできます。</span><span class="sxs-lookup"><span data-stu-id="5c4a6-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="5c4a6-106">価格調整と割引のどちらも、価格グループとリンクすることができます。</span><span class="sxs-lookup"><span data-stu-id="5c4a6-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="5c4a6-107">価格調整と割引の両方について、単一の開始日と終了日を指定するか、または期間コード、割引コード、その他の追加の属性を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="5c4a6-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="5c4a6-108">価格調整と割引は、製品、バリアント、またはカテゴリーに適用できます。</span><span class="sxs-lookup"><span data-stu-id="5c4a6-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="5c4a6-109">複数の割引が製品に適用される場合、割引コンフィギュレーションの設定によって、顧客はいずれか 1 つの割引、または複合された割引を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="5c4a6-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="5c4a6-110">コマースでは、割引または複合割引を、顧客に最適な価格となるように自動的に適用します。</span><span class="sxs-lookup"><span data-stu-id="5c4a6-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="5c4a6-111">価格調整または割引を設定する場合、価格グループが、割引が適用される正しいチャンネル、カタログ、所属、またはロイヤルティ プログラムに割り当てられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5c4a6-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="5c4a6-112">また、割引 ID を自動的に生成するには、新しい割引または価格調整を定義する前に、**コマース パラメーター** ページで番号順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="5c4a6-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="5c4a6-113">価格調整または割引を削除できます。</span><span class="sxs-lookup"><span data-stu-id="5c4a6-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="5c4a6-114">ただし、統計情報は失われます。</span><span class="sxs-lookup"><span data-stu-id="5c4a6-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="5c4a6-115">割引タイプ</span><span class="sxs-lookup"><span data-stu-id="5c4a6-115">Types of discounts</span></span>

<span data-ttu-id="5c4a6-116">割引には多くのタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="5c4a6-116">There are many types of discounts:</span></span>

- <span data-ttu-id="5c4a6-117">**単純割引** – 単一のパーセントまたは量。</span><span class="sxs-lookup"><span data-stu-id="5c4a6-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="5c4a6-118">**数量割引** – 複数の製品を購入するときに適用される割引。</span><span class="sxs-lookup"><span data-stu-id="5c4a6-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="5c4a6-119">**組み合わせ割引** – 顧客が特定の製品の組み合わせを購入した場合に提供される割引。</span><span class="sxs-lookup"><span data-stu-id="5c4a6-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="5c4a6-120">**しきい値割引** – トランザクションの合計が指定金額より大きいときに適用される割引。</span><span class="sxs-lookup"><span data-stu-id="5c4a6-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>
- <span data-ttu-id="5c4a6-121">**支払/入金ベースの割引** – トランザクションの合計が指定した金額を超えて、特定の支払タイプ (現金、貸方、またはデビット カードなど) が支払に使用された場合に適用される割引。</span><span class="sxs-lookup"><span data-stu-id="5c4a6-121">**Tender-based discount** – A discount that is applied when the transaction total is more than a specified amount and a specific payment type (for example, cash, credit, or debit card) is used for payment.</span></span>
- <span data-ttu-id="5c4a6-122">**送料割引** – トランザクションの合計が指定した金額を超えて、特定の荷渡方法 (出荷または一括出荷) が注文で使用される場合に適用される割引。</span><span class="sxs-lookup"><span data-stu-id="5c4a6-122">**Shipping discount** – A discount that is applied when the transaction total is more than a specified amount and a specific mode of delivery (for example, two day shipping or overnight shipping) is used on the order.</span></span>

<span data-ttu-id="5c4a6-123">価格調整と割引のどちらも、価格グループと関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="5c4a6-123">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="5c4a6-124">価格グループは、チャンネル、カタログ、加盟者およびロイヤルティ プログラムに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="5c4a6-124">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]