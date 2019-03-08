---
title: 製造品目の固定費の償却
description: 製造品目の固定費は、工程の段取り時間と、数量または仕損金額が一定のコンポーネントを反映します。
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 7ccd5ce3e2ed58db8f13eebbcfa6fe5fb544d6c7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "329462"
---
# <a name="amortize-constant-costs-for-a-manufactured-item"></a><span data-ttu-id="b5ab9-103">製造品目の固定費の償却</span><span class="sxs-lookup"><span data-stu-id="b5ab9-103">Amortize constant costs for a manufactured item</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5ab9-104">製造品目の固定費は、工程の段取り時間と、数量または仕損金額が一定のコンポーネントを反映します。</span><span class="sxs-lookup"><span data-stu-id="b5ab9-104">A manufactured item’s constant costs reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span> 

<span data-ttu-id="b5ab9-105">製造品目の算出原価の中でこれらの固定費を償却するために、原価ロット サイズという概念が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b5ab9-105">The concept of a costing lot size is used to amortize these constant costs in the calculated cost of a manufactured item.</span></span> <span data-ttu-id="b5ab9-106">この概念には複数の同義語があり、その 1 つが会計ロット サイズです。</span><span class="sxs-lookup"><span data-stu-id="b5ab9-106">This concept has several synonyms, one of which is accounting lot size.</span></span> <span data-ttu-id="b5ab9-107">固定費の償却という概念にもさまざまな同義語があり、その 1 つが比例固定費です。</span><span class="sxs-lookup"><span data-stu-id="b5ab9-107">The concept of amortizing constant costs also has several synonyms, one of which is proportional constant costs.</span></span>

<span data-ttu-id="b5ab9-108">製造品目の原価ロット サイズ数量は、部品表 (BOM) 計算で使用されます。</span><span class="sxs-lookup"><span data-stu-id="b5ab9-108">The quantity of a costing lot size for a manufactured item is used in a bill of material (BOM) calculation.</span></span> <span data-ttu-id="b5ab9-109">この数量は、次に説明するように、BOM 計算を開始および実行する方法によって異なります:</span><span class="sxs-lookup"><span data-stu-id="b5ab9-109">The quantity depends on how you initiate and perform the BOM calculation, as illustrated by the following:</span></span>

-   <span data-ttu-id="b5ab9-110">品目の BOM 計算における既定の計算量 − 在庫用の品目の標準注文数量は、原価ロット サイズとして機能しますが、この既定値は、品目の注文数量の倍数を反映する大きな数量になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b5ab9-110">Default calculation quantity in an item’s BOM calculation − The item’s standard order quantity for inventory acts as the costing lot size, but the default value might be a greater quantity to reflect the item’s order quantity multiple.</span></span> <span data-ttu-id="b5ab9-111">品目の標準注文数量と倍数は、既定の注文設定またはサイト固有の注文設定の中に定義できます。</span><span class="sxs-lookup"><span data-stu-id="b5ab9-111">The item’s standard order quantity and multiple can be defined within its default order settings or site-specific order settings.</span></span>
-   <span data-ttu-id="b5ab9-112">品目の BOM 計算における指定された計算量 : 指定された計算量は、品目の原価ロット サイズとして機能します。</span><span class="sxs-lookup"><span data-stu-id="b5ab9-112">Specified calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item.</span></span> <span data-ttu-id="b5ab9-113">計算量は、最初は、品目の標準注文数量が使用されますが、手動で上書きできます。</span><span class="sxs-lookup"><span data-stu-id="b5ab9-113">The calculation quantity initially uses the item’s standard order quantity, but the default value can be manually overridden.</span></span> <span data-ttu-id="b5ab9-114">指定された計算量は、指定した品目と、生産の BOM 明細行タイプがある製造コンポーネントの原価ロット サイズを表します。</span><span class="sxs-lookup"><span data-stu-id="b5ab9-114">The specified calculation quantity represents the costing lot size for the specified item, and for manufactured components that have a BOM line type of production.</span></span> <span data-ttu-id="b5ab9-115">これは、コンポーネントが正確な数量で生産されることが前提となっているためです。</span><span class="sxs-lookup"><span data-stu-id="b5ab9-115">This is because it is assumed that the component will be produced to the exact quantity.</span></span> <span data-ttu-id="b5ab9-116">品目が BOM 明細行タイプであるその他の製造コンポーネントの原価ロット サイズは、それぞれの標準注文数量を反映します。</span><span class="sxs-lookup"><span data-stu-id="b5ab9-116">The costing lot size for other manufactured components that have a BOM line type of item will reflect their standard order quantity.</span></span>
-   <span data-ttu-id="b5ab9-117">品目の BOM 計算における指定された受注生産計算量 : 指定された計算量は、BOM 計算で受注生産展開モードが使用される場合の品目と製造コンポーネントの原価ロット サイズとして機能します。</span><span class="sxs-lookup"><span data-stu-id="b5ab9-117">Specified make-to-order calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item and its manufactured components when BOM calculations use a make-to-order explosion mode.</span></span> <span data-ttu-id="b5ab9-118">製造コンポーネントは、生産が BOM 明細行タイプの製造コンポーネントと同じように、正確な数量で生産されるということが前提になっています。</span><span class="sxs-lookup"><span data-stu-id="b5ab9-118">It is assumed that the manufactured components will be produced to the exact quantity, just like a manufactured component that has a BOM line type of production.</span></span>
-   <span data-ttu-id="b5ab9-119">注文固有の BOM 計算における指定された計算量 : 注文固有の BOM 計算は、販売注文、販売見積、またはサービス注文の品目に対して実行できます。</span><span class="sxs-lookup"><span data-stu-id="b5ab9-119">Specified calculation quantity in an order-specific BOM calculation − An order-specific BOM calculation can be performed for a line item on a sales order, sales quotation, or service order.</span></span> <span data-ttu-id="b5ab9-120">指定された計算量では元の明細行品目の数量が使用されますが、この既定の数量は上書きできます。</span><span class="sxs-lookup"><span data-stu-id="b5ab9-120">The specified calculation quantity uses the quantity on the originating line item, but the default quantity can be overridden.</span></span> <span data-ttu-id="b5ab9-121">注文固有の BOM 計算では、受注生産とマルチレベル展開モードのどちらを使用するかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="b5ab9-121">You can select whether the order-specific BOM calculation uses a make-to-order or multilevel explosion mode.</span></span>

<span data-ttu-id="b5ab9-122">製造品目の償却される固定費の計算金額は雑費と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="b5ab9-122">The calculated amount of a manufactured item’s amortized constant costs is termed charges.</span></span>





