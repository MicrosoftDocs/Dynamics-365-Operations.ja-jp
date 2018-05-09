---
title: "価格調整および割引"
description: "この記事では、Microsoft Dynamics 365 for Retail での価格調整と割引に関する情報を提供します。"
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 04fd3b3df2637f897d4c25681d00d3700517b070
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="6434a-103">価格調整および割引</span><span class="sxs-lookup"><span data-stu-id="6434a-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6434a-104">この記事では、Microsoft Dynamics 365 for Retail での価格調整と割引に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="6434a-104">This article provides information about price adjustments and discounts in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="6434a-105">Dynamics 365 for Retail では、コール センターの販売注文またはオンライン注文について、製品の価格調整を行ったり、および明細行品目またはトランザクションに POS (販売時点管理) で適用される割引を設定できます。</span><span class="sxs-lookup"><span data-stu-id="6434a-105">In Dynamics 365 for Retail, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="6434a-106">価格調整と割引のどちらも、価格グループとリンクすることができます。</span><span class="sxs-lookup"><span data-stu-id="6434a-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="6434a-107">価格調整と割引の両方について、単一の開始日と終了日を指定するか、または期間コード、割引コード、その他の追加の属性を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="6434a-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> <span data-ttu-id="6434a-108">価格調整と割引は、製品、バリアント、またはカテゴリーに適用できます。</span><span class="sxs-lookup"><span data-stu-id="6434a-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="6434a-109">複数の割引が製品に適用される場合、割引コンフィギュレーションの設定によって、顧客はいずれか 1 つの割引、または複合された割引を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="6434a-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="6434a-110">Dynamics 365 for Retail では、割引または複合割引を、顧客に最適な価格となるように自動的に適用します。</span><span class="sxs-lookup"><span data-stu-id="6434a-110">Dynamics 365 for Retail automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="6434a-111">価格調整または割引を設定する場合、価格グループが、割引が適用される正しいチャンネル、カタログ、所属、またはロイヤルティ プログラムに割り当てられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6434a-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="6434a-112">また、割引 ID を自動的に生成するには、新しい割引または価格調整を定義する前に、**小売パラメーター** ページで番号順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="6434a-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Retail parameters** page before you define a new price adjustment or discount.</span></span> <span data-ttu-id="6434a-113">**注記:** 価格調整または割引を削除できます。</span><span class="sxs-lookup"><span data-stu-id="6434a-113">**Note:** You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="6434a-114">ただし、統計情報は失われます。</span><span class="sxs-lookup"><span data-stu-id="6434a-114">However, statistical information will be lost.</span></span>

### <a name="types-of-discounts"></a><span data-ttu-id="6434a-115">割引タイプ</span><span class="sxs-lookup"><span data-stu-id="6434a-115">Types of discounts</span></span>

<span data-ttu-id="6434a-116">小売割引には次の 4 タイプがあります。</span><span class="sxs-lookup"><span data-stu-id="6434a-116">There are four types of retail discounts:</span></span>

-   <span data-ttu-id="6434a-117">**単純割引** – 単一のパーセントまたは量。</span><span class="sxs-lookup"><span data-stu-id="6434a-117">**Simple discount** – A single percentage or amount.</span></span>
-   <span data-ttu-id="6434a-118">**数量割引** – 複数の製品を購入するときに適用される割引。</span><span class="sxs-lookup"><span data-stu-id="6434a-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
-   <span data-ttu-id="6434a-119">**組み合わせ割引** – 顧客が特定の製品の組み合わせを購入した場合に提供される割引。</span><span class="sxs-lookup"><span data-stu-id="6434a-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
-   <span data-ttu-id="6434a-120">**しきい値割引** – トランザクションの合計が指定金額より大きいときに適用される割引。</span><span class="sxs-lookup"><span data-stu-id="6434a-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>

<span data-ttu-id="6434a-121">価格調整と割引のどちらも、価格グループと関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="6434a-121">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="6434a-122">価格グループは、チャンネル、カタログ、加盟者およびロイヤルティ プログラムに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="6434a-122">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>




