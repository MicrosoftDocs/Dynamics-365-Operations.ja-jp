---
title: "現物価格を含める"
description: "[品目モデル グループ] ページの [在庫モデル] クイックタブにある [現物価格を含める] チェック ボックスは、物理的に更新された取引を品目の平均原価価格を計算するときに考慮するかどうかを指定するために使用されます。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4ea8fe31588dd0768e0651c9e1e332212a00cde2
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="include-physical-value"></a><span data-ttu-id="8ffe9-103">現物価格を含める</span><span class="sxs-lookup"><span data-stu-id="8ffe9-103">Include physical value</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8ffe9-104">[品目モデル グループ] ページの [在庫モデル] クイックタブにある [現物価格を含める] チェック ボックスは、物理的に更新された取引を品目の平均原価価格を計算するときに考慮するかどうかを指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8ffe9-104">You use the Include physical value check box on the Inventory model FastTab of the Item model groups page to specify whether physically updated transactions are considered when the running average cost price is calculated for an item.</span></span>

<span data-ttu-id="8ffe9-105">[**現物価格を含める**] チェック ボックスには、次の値があります。</span><span class="sxs-lookup"><span data-stu-id="8ffe9-105">The **Include physical value** check box has the following values.</span></span>

| <span data-ttu-id="8ffe9-106">値</span><span class="sxs-lookup"><span data-stu-id="8ffe9-106">Value</span></span>    | <span data-ttu-id="8ffe9-107">結果</span><span class="sxs-lookup"><span data-stu-id="8ffe9-107">Result</span></span>                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ffe9-108">選択済</span><span class="sxs-lookup"><span data-stu-id="8ffe9-108">Selected</span></span> | <span data-ttu-id="8ffe9-109">物理的に更新された取引と財務上で更新された取引の両方を使用して、平均原価価格が計算されます。</span><span class="sxs-lookup"><span data-stu-id="8ffe9-109">Both physically updated transactions and financially updated transactions are used to calculate the running average cost price.</span></span> |
| <span data-ttu-id="8ffe9-110">オフ</span><span class="sxs-lookup"><span data-stu-id="8ffe9-110">Cleared</span></span>  | <span data-ttu-id="8ffe9-111">財務上で更新された取引だけを使用して、平均原価価格が計算されます。</span><span class="sxs-lookup"><span data-stu-id="8ffe9-111">Only financially updated transactions are used to calculate the running average cost price.</span></span>                                     |

<span data-ttu-id="8ffe9-112">使用する在庫モデルに応じて、チェック ボックスの効果が少し異なります。</span><span class="sxs-lookup"><span data-stu-id="8ffe9-112">The check box has slightly different effects, depending on the inventory model that you use.</span></span>

-   <span data-ttu-id="8ffe9-113">FIFO (先入れ先出し)、LIFO (後入れ先出し)、または LIFO 日付在庫モデルを使用しているときに [**現物価格を含める**] チェック ボックスをオンにした場合、在庫原価計算では、物理的に更新された取引も調整されます。</span><span class="sxs-lookup"><span data-stu-id="8ffe9-113">If you select the **Include physical value** check box when you use the FIFO (First in, first out), LIFO (Last in, first out), or LIFO date inventory model, inventory close also makes adjustments to physically updated transactions.</span></span>
-   <span data-ttu-id="8ffe9-114">これらの在庫モデルを使用しているときに [**現物価格を含める**] チェック ボックスをオンにしなかった場合、在庫原価計算では、財務上更新された取引に対してのみ決済が行われます。</span><span class="sxs-lookup"><span data-stu-id="8ffe9-114">If you don't select the **Include physical value** check box when you use these inventory models, inventory close makes settlements only to financially updated transactions.</span></span>
-   <span data-ttu-id="8ffe9-115">加重平均または加重平均日付在庫モデルを使用している場合、在庫原価計算では、[**現物価格を含める**] チェック ボックスがオンかオフかに関係なく、財務上で更新された取引だけが決済されます。</span><span class="sxs-lookup"><span data-stu-id="8ffe9-115">When you use the weighted average or weighted average date inventory model, inventory close settles only financially updated transactions, regardless of whether you select the **Include physical value** check box.</span></span>

<span data-ttu-id="8ffe9-116">**例 1** [**現物価格を含める**] チェック ボックスをオンにして、次の発注を受信した場合。</span><span class="sxs-lookup"><span data-stu-id="8ffe9-116">**Example 1** You've selected the **Include physical value** check box and receive the following purchase orders:</span></span>

-   <span data-ttu-id="8ffe9-117">梱包明細に反映済の、原価価格が USD 10.00 で数量が 2 の発注書</span><span class="sxs-lookup"><span data-stu-id="8ffe9-117">A purchase order for a quantity of 2 and a cost price of USD 10.00 that has been packing slip–updated</span></span>
-   <span data-ttu-id="8ffe9-118">請求書に反映済の、原価価格が USD 12.00 で数量が 3 の発注書</span><span class="sxs-lookup"><span data-stu-id="8ffe9-118">A purchase order for a quantity of 3 and a cost price of USD 12.00 that has been invoice-updated</span></span>

<span data-ttu-id="8ffe9-119">この場合、原価価格は、物理的に更新された取引と財務上で更新された取引の両方を使用して計算されるため、平均原価価格は USD 11.20 になります。</span><span class="sxs-lookup"><span data-stu-id="8ffe9-119">In this case, the running average cost price will be USD 11.20, because both physically updated transactions and financially updated transactions are used to calculate the cost price.</span></span> <span data-ttu-id="8ffe9-120">**例 2** [**現物価格を含める**] チェック ボックスをオフにし、品目設定の原価価格が USD 10.00 の場合。</span><span class="sxs-lookup"><span data-stu-id="8ffe9-120">**Example 2** You haven't selected the **Include physical value** check box, and the cost price on the item setup is USD 10.00.</span></span> <span data-ttu-id="8ffe9-121">梱包明細に反映済の、原価価格が USD 12.00 で数量が 20 の発注書を入荷します。</span><span class="sxs-lookup"><span data-stu-id="8ffe9-121">You receive a purchase order for a quantity of 20 and a cost price of USD 12.00 that has been packing slip–updated.</span></span> <span data-ttu-id="8ffe9-122">物理的に転記された取引は平均原価価格には含まれないため、販売注文が転記されるときに、転記される原価金額は USD 10.00 になります。</span><span class="sxs-lookup"><span data-stu-id="8ffe9-122">When a sales order is posted, the posted cost amount is USD 10.00, because the running average cost price won't include physically posted transactions.</span></span> <span data-ttu-id="8ffe9-123">**メモ:** これに対して、この品目の [**現物価格を含める**] チェック ボックスをオンにすると、販売注文が転記されるときに転記された原価金額が USD 12.00 となります。</span><span class="sxs-lookup"><span data-stu-id="8ffe9-123">**Note:** For comparison, if you select the **Include physical value** check box for this item, when a sales order is posted, the posted cost amount will be USD 12.00.</span></span>




