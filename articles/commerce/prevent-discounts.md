---
title: 小売製品の割引を禁止するためのオプション
description: 小売業者はさまざまな理由で、一部の製品の割引を、プロモーションからまたは POS での販売中に禁止します。
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: ddf3834057c89f5a091f09412183ca79540225fc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802890"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a><span data-ttu-id="447aa-103">小売製品の割引を禁止するためのオプション</span><span class="sxs-lookup"><span data-stu-id="447aa-103">Options for preventing discounts for retail products</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="447aa-104">小売業者はさまざまな理由で、一部の製品の割引を、プロモーションからまたは POS での販売中に禁止します。</span><span class="sxs-lookup"><span data-stu-id="447aa-104">There are various reasons why retailers may want to prevent some products from being discounted, either from a promotion or during the sale at the POS.</span></span>

<span data-ttu-id="447aa-105">リリース済製品の **コマース** タブ上で表示される次のオプションで、すべてのまたは手動の割引を禁止するよう製品をコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="447aa-105">The following options, which can be found on the **Commerce** tab of released products, will allow the product to be configured to prevent all or manual discounts.</span></span> <span data-ttu-id="447aa-106">その設定は、カテゴリ階層からカテゴリ レベルで指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="447aa-106">The settings can also be specified at the category level from the category hierarchy.</span></span>

- <span data-ttu-id="447aa-107">**すべての割引を禁止** – すべてのタイプの割引をこの製品に適用禁止にするには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="447aa-107">**Prevent all discounts** – Select this option to prevent all types of discounts from being applied to this product.</span></span> <span data-ttu-id="447aa-108">これには、組み合わせ、数量およびしきい値割引などのプロモーション、また POS ユーザーによる販売中に適用される手動の明細行およびトランザクションの割引が含まれます。</span><span class="sxs-lookup"><span data-stu-id="447aa-108">This includes promotions such as mix and match, quantity and threshold discounts, as well as manual line and transaction discounts that are applied during a sale by a POS user.</span></span>
- <span data-ttu-id="447aa-109">**手動の割引を禁止** – POS ユーザーによる販売中に適用される手動の明細行またはトランザクションの割引のみを禁止するには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="447aa-109">**Prevent manual discounts** – Select this option to only prevent the manual line or transaction discounts that are applied during a sale by a POS user.</span></span> <span data-ttu-id="447aa-110">このオプションを選択した製品は、組み合わせ、数量およびしきい値割引などのプロモーションについてはまだ対象となっています。</span><span class="sxs-lookup"><span data-stu-id="447aa-110">Products with this option selected are still eligible for promotions, such as mix and match and quantity and threshold discounts.</span></span>

> [!NOTE]
> <span data-ttu-id="447aa-111">価格上書き操作は、基準価格の設定をするもので割引としては扱われないので、これらの設定によって制限されません。</span><span class="sxs-lookup"><span data-stu-id="447aa-111">These settings do not restrict the price override operation, because that sets the base price and is not treated as a discount.</span></span>

<span data-ttu-id="447aa-112">[![割引フィールドの禁止](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span><span class="sxs-lookup"><span data-stu-id="447aa-112">[![Prevent discounts field](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]