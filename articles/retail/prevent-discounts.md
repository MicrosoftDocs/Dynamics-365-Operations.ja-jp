---
title: "小売製品の割引を禁止するためのオプション"
description: "小売業者はさまざまな理由で、一部の製品の割引を、プロモーションからまたは POS での販売中に禁止します。"
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: eaee79e2a20ab443cf3779e8499bf29d63ad3dfc
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2018

---

# <a name="options-for-preventing-discounts-for-retail-products"></a><span data-ttu-id="3f484-103">小売製品の割引を禁止するためのオプション</span><span class="sxs-lookup"><span data-stu-id="3f484-103">Options for preventing discounts for retail products</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3f484-104">小売業者はさまざまな理由で、一部の製品の割引を、プロモーションからまたは POS での販売中に禁止します。</span><span class="sxs-lookup"><span data-stu-id="3f484-104">There are various reasons why retailers may want to prevent some products from being discounted, either from a promotion or during the sale at the POS.</span></span>

<span data-ttu-id="3f484-105">リリース済製品の**小売**タブ上で表示される次のオプションで、すべてのまたは手動の割引を禁止するよう製品をコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="3f484-105">The following options, which can be found on the **Retail** tab of released products, will allow the product to be configured to prevent all or manual discounts.</span></span> <span data-ttu-id="3f484-106">その設定は、小売カテゴリ階層からカテゴリ レベルで指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="3f484-106">The settings can also be specified at the category level from the retail category hierarchy.</span></span>

<span data-ttu-id="3f484-107">**すべての割引を禁止**: すべてのタイプの割引をこの製品に適用禁止にするには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="3f484-107">**Prevent all discounts**: Select this option to prevent all types of discounts from being applied to this product.</span></span> <span data-ttu-id="3f484-108">これには、組み合わせ、数量およびしきい値割引などのプロモーション、また POS ユーザーによる販売中に適用される手動の明細行およびトランザクションの割引が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3f484-108">This includes promotions such as mix and match, quantity and threshold discounts, as well as manual line and transaction discounts that are applied during a sale by a POS user.</span></span>

<span data-ttu-id="3f484-109">**手動の割引を禁止**: POS ユーザーによる販売中に適用される手動の明細行またはトランザクションの割引のみを禁止するには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="3f484-109">**Prevent manual discounts**: Select this option to only prevent the manual line or transaction discounts that are applied during a sale by a POS user.</span></span> <span data-ttu-id="3f484-110">このオプションを選択した製品は、組み合わせ、数量およびしきい値割引などのプロモーションについてはまだ対象となっています。</span><span class="sxs-lookup"><span data-stu-id="3f484-110">Products with this option selected are still eligible for promotions, such as mix and match and quantity and threshold discounts.</span></span>

<span data-ttu-id="3f484-111">**注記**: 価格上書き操作は、基準価格の設定をするもので割引としては扱われないので、これらの設定によって制限されません。</span><span class="sxs-lookup"><span data-stu-id="3f484-111">**Note**: These settings do not restrict the price override operation, because that sets the base price and is not treated as a discount.</span></span>  

<span data-ttu-id="3f484-112">[![割引フィールドの禁止](./media/prevent discounts.png)](./media/prevent discounts.png)</span><span class="sxs-lookup"><span data-stu-id="3f484-112">[![prevent discounts field](./media/prevent discounts.png)](./media/prevent discounts.png)</span></span>

