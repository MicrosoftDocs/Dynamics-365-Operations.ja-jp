---
title: "分析コードの作成と分析コード メンバーのインポート"
description: "原価会計は、他のモジュールからのマスター データを必要とする独立モジュールです。"
author: ShylaThompson
manager: AnnBe
ms.date: 09/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: d48ba0a0b80d251e107baa0ceeb66d8e328f13dc
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---

# <a name="create-dimensions-and-import-dimension-members"></a><span data-ttu-id="c5141-103">分析コードの作成と分析コード メンバーのインポート</span><span class="sxs-lookup"><span data-stu-id="c5141-103">Create dimensions and import dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c5141-104">原価会計は、他のモジュールからのデータを必要とする独立モジュールです。</span><span class="sxs-lookup"><span data-stu-id="c5141-104">Cost accounting is an independent module that requires data from other modules.</span></span> <span data-ttu-id="c5141-105">このデータは、次のように分類されます。</span><span class="sxs-lookup"><span data-stu-id="c5141-105">This data is categorized into the following:</span></span>

-  <span data-ttu-id="c5141-106">コスト要素</span><span class="sxs-lookup"><span data-stu-id="c5141-106">Cost elements</span></span>
-  <span data-ttu-id="c5141-107">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="c5141-107">Cost objects</span></span>
-  <span data-ttu-id="c5141-108">統計分析コード</span><span class="sxs-lookup"><span data-stu-id="c5141-108">Statistical dimensions</span></span>

<span data-ttu-id="c5141-109">**原価要素**は、勘定科目表で原価関連品目に対応します。</span><span class="sxs-lookup"><span data-stu-id="c5141-109">A **Cost element** corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="c5141-110">**原価オブジェクト**は、製品、コスト センター、またプロジェクトといった、見積したり、原価を割り当てたり、直接測定したりする財務分析コードのすべてのタイプに対応します。</span><span class="sxs-lookup"><span data-stu-id="c5141-110">A **Cost object** corresponds to any type of financial dimension, such as products, cost centers, and projects that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="c5141-111">**統計分析コード**とそのメンバーは、非通貨入力を登録するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c5141-111">A **Statistical dimension** and its members are used to register non-monetary entries.</span></span> <span data-ttu-id="c5141-112">統計分析コード メンバーは、コスト配分や配賦の配賦基準として使用できます。</span><span class="sxs-lookup"><span data-stu-id="c5141-112">Statistical dimension members can be used as an allocation base in cost distribution and allocation</span></span> 

<span data-ttu-id="c5141-113">次の図は、原価会計で使用される分析コードを示します。</span><span class="sxs-lookup"><span data-stu-id="c5141-113">The following diagram illustrates the dimensions that are used in Cost accounting.</span></span>

<span data-ttu-id="c5141-114">[![原価会計分析コード](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="c5141-114">[![Cost accounting dimensions](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span></span>

<span data-ttu-id="c5141-115">原価会計にデータをインポートすると、組織のすべてのレベルでマネージャーに洞察を提供するさまざまな分析視点を構築するためにそのデータを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="c5141-115">After the data is imported into Cost accounting, you can use it to build various perspectives that provide insights to managers at all levels of the organization.</span></span> <span data-ttu-id="c5141-116">以下のトピックでは、分析コードの作成および分析コード メンバーのインポートに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="c5141-116">The following topics provide information about creating dimensions and importing dimension members.</span></span> 

-  [<span data-ttu-id="c5141-117">原価要素分析コード</span><span class="sxs-lookup"><span data-stu-id="c5141-117">Cost element dimensions</span></span>](cost-elements.md)
-  [<span data-ttu-id="c5141-118">原価要素の作成 (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="c5141-118">Create cost elements (Task guide)</span></span>](./tasks/create-cost-elements.md)
-  [<span data-ttu-id="c5141-119">原価オブジェクト分析コード</span><span class="sxs-lookup"><span data-stu-id="c5141-119">Cost object dimensions</span></span>](cost-objects.md)
-  [<span data-ttu-id="c5141-120">原価要素の作成 (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="c5141-120">Create cost elements (Task guide)</span></span>](./tasks/create-cost-objects.md)
-  [<span data-ttu-id="c5141-121">分析コード メンバーの共通セットに対する原価要素分析コード メンバーのマップ</span><span class="sxs-lookup"><span data-stu-id="c5141-121">Map cost element dimension members to a common set of dimension members</span></span>](map-cost-elements-dimension-members.md)
-  [<span data-ttu-id="c5141-122">原価要素分析コードのマップ (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="c5141-122">Map a cost element dimension (Task guide)</span></span>](./tasks/map-cost-element-dimension.md)
-  [<span data-ttu-id="c5141-123">統計分析コード メンバーと統計測定プロバイダー テンプレート</span><span class="sxs-lookup"><span data-stu-id="c5141-123">Statistical dimension members and statistical measure provider templates</span></span>](statistical-measure-provider-template.md)







