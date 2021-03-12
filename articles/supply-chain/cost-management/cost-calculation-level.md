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
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 42088d8c005cf3fc04e768f1b8e8c8ca0b8c6993
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967735"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="0f1dc-104">原価計算レベル</span><span class="sxs-lookup"><span data-stu-id="0f1dc-104">Cost calculation level</span></span>

<span data-ttu-id="0f1dc-105">**原価計算レベル** が指定された部品表 (BOM) レベルでは、計算から製造注文とバッチ注文が除外されます。</span><span class="sxs-lookup"><span data-stu-id="0f1dc-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="0f1dc-106">このシステムは、原価計算のバージョンで原価計算を実行する際に、このレベルを使用します。</span><span class="sxs-lookup"><span data-stu-id="0f1dc-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="0f1dc-107">再計算や在庫原価計算などのプロセスでは、システムは代わりに **原価計算レベル** の BOM レベルを使用します。</span><span class="sxs-lookup"><span data-stu-id="0f1dc-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="0f1dc-108">以下の簡単なシナリオでは、**原価計算レベル** の  BOM レベルと **原価レベル** の BOM レベルの違いを示しています。</span><span class="sxs-lookup"><span data-stu-id="0f1dc-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="0f1dc-109">ここでは、A、B、C の 3 つの製品が使用されます。製品 C は製品 B のコンポーネントで、製品 B は製品 A のコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="0f1dc-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="0f1dc-110">**原価レベル** では、次の BOM レベルが割り当てられます :</span><span class="sxs-lookup"><span data-stu-id="0f1dc-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="0f1dc-111">**製品 A :** 0</span><span class="sxs-lookup"><span data-stu-id="0f1dc-111">**Product A:** 0</span></span>
    - <span data-ttu-id="0f1dc-112">**製品 B :** 1</span><span class="sxs-lookup"><span data-stu-id="0f1dc-112">**Product B:** 1</span></span>
    - <span data-ttu-id="0f1dc-113">**製品 C :** 2</span><span class="sxs-lookup"><span data-stu-id="0f1dc-113">**Product C:** 2</span></span>

- <span data-ttu-id="0f1dc-114">**原価計算レベル** では、次の BOM レベルが割り当てられます :</span><span class="sxs-lookup"><span data-stu-id="0f1dc-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="0f1dc-115">**製品 A :** 0</span><span class="sxs-lookup"><span data-stu-id="0f1dc-115">**Product A:** 0</span></span>
    - <span data-ttu-id="0f1dc-116">**製品 B :** 1</span><span class="sxs-lookup"><span data-stu-id="0f1dc-116">**Product B:** 1</span></span>
    - <span data-ttu-id="0f1dc-117">**製品 C :** 2</span><span class="sxs-lookup"><span data-stu-id="0f1dc-117">**Product C:** 2</span></span>

<span data-ttu-id="0f1dc-118">製品 C の製造オーダーが作成され、製品 A が製造オーダー BOM に追加されます。</span><span class="sxs-lookup"><span data-stu-id="0f1dc-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="0f1dc-119">注文の見積後、BOM レベルは次のように更新されます :</span><span class="sxs-lookup"><span data-stu-id="0f1dc-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="0f1dc-120">**原価レベル** では、次の BOM レベルが割り当てられます :</span><span class="sxs-lookup"><span data-stu-id="0f1dc-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="0f1dc-121">**製品 B :** 1</span><span class="sxs-lookup"><span data-stu-id="0f1dc-121">**Product B:** 1</span></span>
    - <span data-ttu-id="0f1dc-122">**製品 C :** 2</span><span class="sxs-lookup"><span data-stu-id="0f1dc-122">**Product C:** 2</span></span>
    - <span data-ttu-id="0f1dc-123">**製品 A :** 3</span><span class="sxs-lookup"><span data-stu-id="0f1dc-123">**Product A:** 3</span></span>

- <span data-ttu-id="0f1dc-124">**原価計算レベル** では、次の BOM レベルが割り当てられます :</span><span class="sxs-lookup"><span data-stu-id="0f1dc-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="0f1dc-125">**製品 A :** 0</span><span class="sxs-lookup"><span data-stu-id="0f1dc-125">**Product A:** 0</span></span>
    - <span data-ttu-id="0f1dc-126">**製品 B :** 1</span><span class="sxs-lookup"><span data-stu-id="0f1dc-126">**Product B:** 1</span></span>
    - <span data-ttu-id="0f1dc-127">**製品 C :** 2</span><span class="sxs-lookup"><span data-stu-id="0f1dc-127">**Product C:** 2</span></span>

<span data-ttu-id="0f1dc-128">この動作により、製造オーダー BOM に対する変更が後続の原価計算に影響を与えることがなくなります。</span><span class="sxs-lookup"><span data-stu-id="0f1dc-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>
