---
title: "製造品目の雑費の表示"
description: "製造品目の固定費は、工程の段取り時間と、数量または仕損金額が固定されているコンポーネントを反映します。"
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 274483
ms.assetid: 6f5b851b-c5a7-43ef-b380-0d316667c1ef
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: fe766a2969e647500452ecb64040d2157a155416
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="display-charges-for-a-manufactured-item"></a><span data-ttu-id="da620-103">製造品目の雑費の表示</span><span class="sxs-lookup"><span data-stu-id="da620-103">Display charges for a manufactured item</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="da620-104">製造品目の固定費は、工程の段取り時間と、数量または仕損金額が固定されているコンポーネントを反映します。</span><span class="sxs-lookup"><span data-stu-id="da620-104">The constant costs of a manufactured item reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span>

<span data-ttu-id="da620-105">品目の請求金額の計算された金額は、品目の単位原価で表示できます。</span><span class="sxs-lookup"><span data-stu-id="da620-105">The calculated amount of an item's charges can be displayed with the item's unit costs.</span></span> <span data-ttu-id="da620-106">ただし、請求金額は、別個のフィールドとして表示され、品目の単位原価には含まれません。</span><span class="sxs-lookup"><span data-stu-id="da620-106">However, the charges are sometimes displayed as separate fields, and they are not included in the item's unit costs.</span></span> <span data-ttu-id="da620-107">請求金額が別個のフィールドとして表示されるとき、1 つのフィールドには請求金額の合計金額が表示され、別のフィールドにはその金額の償却に使用される原価ロット サイズが表示されます。</span><span class="sxs-lookup"><span data-stu-id="da620-107">When the charges appear as separate fields, one field displays the total amount of charges, and another field displays the costing lot size that is used to amortize the amount.</span></span> <span data-ttu-id="da620-108">たとえば、品目価格ページには、請求金額が 2 つの別個のフィールドとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="da620-108">The Item price page, for example, displays the charges as two separate fields.</span></span> <span data-ttu-id="da620-109">ただし、完了ページには品目の単位あたりの合計原価が表示され、償却原価が単位原価に含まれます。</span><span class="sxs-lookup"><span data-stu-id="da620-109">However, the Complete page displays the item's total cost per unit, and the amortized costs are included in the unit costs.</span></span>

<span data-ttu-id="da620-110">製造品目の請求金額は、常に、標準費目別原価に対する品目の単位原価に含まれます。</span><span class="sxs-lookup"><span data-stu-id="da620-110">The charges for a manufactured item are always included in the item's unit cost for standard cost purposes.</span></span> <span data-ttu-id="da620-111">必要に応じて、計画費目別原価に含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="da620-111">They can optionally be included for planned cost purposes.</span></span> <span data-ttu-id="da620-112">原価バージョン内のポリシーにより、製造品目の原価に請求金額が含まれます。</span><span class="sxs-lookup"><span data-stu-id="da620-112">A policy in the costing version enforces the inclusion of charges in the cost of a manufactured item.</span></span> <span data-ttu-id="da620-113">品目の原価レコードを有効にすると、品目価格ページに表示されるように、品目の基準原価情報に対する請求金額が更新されます。</span><span class="sxs-lookup"><span data-stu-id="da620-113">When you activate an item's cost record, you update the charges for the item's base cost information, which is displayed in the Item price page.</span></span> <span data-ttu-id="da620-114">ただし、請求金額は、2 つの別個のフィールドとして表示され、品目の単位原価には含まれません。</span><span class="sxs-lookup"><span data-stu-id="da620-114">The charges are displayed as two separate fields, and they are not included in the item's unit cost.</span></span> <span data-ttu-id="da620-115">有効化が異なるサイトを反映するものであっても、有効化のたびに品目の基準原価情報が更新されます。</span><span class="sxs-lookup"><span data-stu-id="da620-115">Each activation updates the item's base cost information, even if the activation reflects different sites.</span></span> <span data-ttu-id="da620-116">したがって、基準原価情報を参照情報として表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="da620-116">Therefore, you should view the base cost information as reference information.</span></span>






