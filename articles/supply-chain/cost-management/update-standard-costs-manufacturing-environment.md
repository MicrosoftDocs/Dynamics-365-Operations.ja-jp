---
title: "製造環境での標準原価を更新"
description: "この記事は、製造環境での標準原価の更新方法についてのガイダンスを提供します。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b9ad13071c3e0c3a294e9d4413de160a58559640
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="update-standard-costs-in-a-manufacturing-environment"></a><span data-ttu-id="94a7e-103">製造環境での標準原価を更新</span><span class="sxs-lookup"><span data-stu-id="94a7e-103">Update standard costs in a manufacturing environment</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="94a7e-104">この記事は、製造環境での標準原価の更新方法についてのガイダンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="94a7e-104">This article provides guidance about how to update standard costs in a manufacturing environment.</span></span> 

<span data-ttu-id="94a7e-105">更新は、新しい品目、コスト カテゴリ、または間接原価計算式を反映する場合があります。</span><span class="sxs-lookup"><span data-stu-id="94a7e-105">Updates can reflect new items, cost categories, or indirect cost calculation formulas.</span></span> <span data-ttu-id="94a7e-106">また、訂正や原価の変化を反映することもできます。</span><span class="sxs-lookup"><span data-stu-id="94a7e-106">They can also reflect corrections and cost changes.</span></span> <span data-ttu-id="94a7e-107">次の例で示すように、更新の種類は、標準原価の更新に必要な手順に影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="94a7e-107">The type of update affects the steps that you must complete to update standard costs, as illustrated in the following cases:</span></span>

-   <span data-ttu-id="94a7e-108">購入品目の予期される標準原価の変更を入力し、適切な日に品目原価レコードのステータスを**有効**に変更します。</span><span class="sxs-lookup"><span data-stu-id="94a7e-108">Enter expected standard cost changes for purchased items, and then change the status of the item cost records to **Active** on the appropriate date.</span></span> <span data-ttu-id="94a7e-109">ただし、購入品目を使用する製造品目の原価は再計算しないでください。</span><span class="sxs-lookup"><span data-stu-id="94a7e-109">However, don't recalculate the costs of manufactured items that use the purchased items.</span></span>
-   <span data-ttu-id="94a7e-110">新しい購入品目の標準原価を入力しますが、新しい購入品目をコンポーネントとして含む部品表 (BOM) バージョンを使用する製造品目の原価は再計算しないでください。</span><span class="sxs-lookup"><span data-stu-id="94a7e-110">Enter standard costs for a new purchased item, but don't recalculate the costs of manufactured items that have a bill of materials (BOM) version that contains the new purchased item as a component.</span></span>
-   <span data-ttu-id="94a7e-111">購入品目の原価を訂正または変更し、または購入品目に割り当てられている原価グループを変更し、購入品目をコンポーネントとして含む BOM バージョンを使用するすべての製造品目の原価を計算します。</span><span class="sxs-lookup"><span data-stu-id="94a7e-111">Correct or change the cost of a purchased item, or change the cost group that is assigned to a purchased item, and calculate the cost for all manufactured items that have a BOM version that contains the purchased item as a component.</span></span>
-   <span data-ttu-id="94a7e-112">原価カテゴリの原価を変更し、その原価カテゴリを使用する工順操作を含む工順バージョンを使用するすべての製造品目の原価を計算します。</span><span class="sxs-lookup"><span data-stu-id="94a7e-112">Change the cost for a cost category, and calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="94a7e-113">工順工程に割り当てられているコスト カテゴリ、またはコスト カテゴリに割り当てられているコスト グループを変更します。</span><span class="sxs-lookup"><span data-stu-id="94a7e-113">Change the cost categories that are assigned to routing operations or the cost group that is assigned to cost categories.</span></span> <span data-ttu-id="94a7e-114">それから、そのコスト カテゴリを使用する工順操作を含む工順バージョンを使用するすべての製造品目のコストを計算します。</span><span class="sxs-lookup"><span data-stu-id="94a7e-114">Then calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="94a7e-115">間接原価計算式を変更し、変更によって影響を受けるすべての製造品目の原価を計算します。</span><span class="sxs-lookup"><span data-stu-id="94a7e-115">Change an indirect cost calculation formula, and calculate the cost for all manufactured items that are affected by the change.</span></span>
-   <span data-ttu-id="94a7e-116">製造品目の製造サイトを変更または追加し、そのサイトに対する品目の製造原価を計算します。</span><span class="sxs-lookup"><span data-stu-id="94a7e-116">Change or add a manufacturing site for a manufactured item, and calculate the item's manufactured cost for the site.</span></span>
-   <span data-ttu-id="94a7e-117">製造品目の原価を計算または再計算し、その製造品目をコンポーネントとして含む BOM バージョンを使用するすべての製造品目の原価を再計算します。</span><span class="sxs-lookup"><span data-stu-id="94a7e-117">Calculate, or recalculate, the cost for a manufactured item, and recalculate the cost for all manufactured items that have a BOM version that contains the manufactured item as a component.</span></span>
-   <span data-ttu-id="94a7e-118">定義済み、承認済みで有効な BOM および工順情報を基にして、新しい製造品目の原価を計算します。</span><span class="sxs-lookup"><span data-stu-id="94a7e-118">Calculate costs for a new manufactured item, based on its defined, approved, and active BOM and route information.</span></span>

<span data-ttu-id="94a7e-119">いずれの場合も、標準原価の更新方法を慎重に検討する必要があります。</span><span class="sxs-lookup"><span data-stu-id="94a7e-119">Each case requires careful consideration about how to update standard costs.</span></span>




