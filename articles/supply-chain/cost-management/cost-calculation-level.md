---
title: 原価計算レベル
description: このトピックでは、原価計算レベルを指定した部品表 (BOM) のレベルについて説明します。 このBOMレベルでは、計算から生産およびバッチ注文は計算から除外されます。
author: AndersGirke
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 52b77e794ee38add556ac01d62c973b38c48a548
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431874"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="4d169-104">原価計算レベル</span><span class="sxs-lookup"><span data-stu-id="4d169-104">Cost calculation level</span></span>

<span data-ttu-id="4d169-105">**原価計算レベル** が指定された部品表 (BOM) レベルでは、計算から製造注文とバッチ注文が除外されます。</span><span class="sxs-lookup"><span data-stu-id="4d169-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="4d169-106">このシステムは、原価計算のバージョンで原価計算を実行する際に、このレベルを使用します。</span><span class="sxs-lookup"><span data-stu-id="4d169-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="4d169-107">再計算や在庫原価計算などのプロセスでは、システムは代わりに **原価計算レベル** の BOM レベルを使用します。</span><span class="sxs-lookup"><span data-stu-id="4d169-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="4d169-108">以下の簡単なシナリオでは、**原価計算レベル** の  BOM レベルと **原価レベル** の BOM レベルの違いを示しています。</span><span class="sxs-lookup"><span data-stu-id="4d169-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="4d169-109">ここでは、A、B、C の 3 つの製品が使用されます。製品 C は製品 B のコンポーネントで、製品 B は製品 A のコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="4d169-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="4d169-110">**原価レベル** では、次の BOM レベルが割り当てられます :</span><span class="sxs-lookup"><span data-stu-id="4d169-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="4d169-111">**製品 A :** 0</span><span class="sxs-lookup"><span data-stu-id="4d169-111">**Product A:** 0</span></span>
    - <span data-ttu-id="4d169-112">**製品 B :** 1</span><span class="sxs-lookup"><span data-stu-id="4d169-112">**Product B:** 1</span></span>
    - <span data-ttu-id="4d169-113">**製品 C :** 2</span><span class="sxs-lookup"><span data-stu-id="4d169-113">**Product C:** 2</span></span>

- <span data-ttu-id="4d169-114">**原価計算レベル** では、次の BOM レベルが割り当てられます :</span><span class="sxs-lookup"><span data-stu-id="4d169-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="4d169-115">**製品 A :** 0</span><span class="sxs-lookup"><span data-stu-id="4d169-115">**Product A:** 0</span></span>
    - <span data-ttu-id="4d169-116">**製品 B :** 1</span><span class="sxs-lookup"><span data-stu-id="4d169-116">**Product B:** 1</span></span>
    - <span data-ttu-id="4d169-117">**製品 C :** 2</span><span class="sxs-lookup"><span data-stu-id="4d169-117">**Product C:** 2</span></span>

<span data-ttu-id="4d169-118">製品 C の製造オーダーが作成され、製品 A が製造オーダー BOM に追加されます。</span><span class="sxs-lookup"><span data-stu-id="4d169-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="4d169-119">注文の見積後、BOM レベルは次のように更新されます :</span><span class="sxs-lookup"><span data-stu-id="4d169-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="4d169-120">**原価レベル** では、次の BOM レベルが割り当てられます :</span><span class="sxs-lookup"><span data-stu-id="4d169-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="4d169-121">**製品 B :** 1</span><span class="sxs-lookup"><span data-stu-id="4d169-121">**Product B:** 1</span></span>
    - <span data-ttu-id="4d169-122">**製品 C :** 2</span><span class="sxs-lookup"><span data-stu-id="4d169-122">**Product C:** 2</span></span>
    - <span data-ttu-id="4d169-123">**製品 A :** 3</span><span class="sxs-lookup"><span data-stu-id="4d169-123">**Product A:** 3</span></span>

- <span data-ttu-id="4d169-124">**原価計算レベル** では、次の BOM レベルが割り当てられます :</span><span class="sxs-lookup"><span data-stu-id="4d169-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="4d169-125">**製品 A :** 0</span><span class="sxs-lookup"><span data-stu-id="4d169-125">**Product A:** 0</span></span>
    - <span data-ttu-id="4d169-126">**製品 B :** 1</span><span class="sxs-lookup"><span data-stu-id="4d169-126">**Product B:** 1</span></span>
    - <span data-ttu-id="4d169-127">**製品 C :** 2</span><span class="sxs-lookup"><span data-stu-id="4d169-127">**Product C:** 2</span></span>

<span data-ttu-id="4d169-128">この動作により、製造オーダー BOM に対する変更が後続の原価計算に影響を与えることがなくなります。</span><span class="sxs-lookup"><span data-stu-id="4d169-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>
