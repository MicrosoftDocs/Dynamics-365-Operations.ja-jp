---
title: 特定の製品ライフサイクル状態の製品を除外する
description: このトピックでは、計画の最適化機能を使用するときに、ライフサイクルの状態に基づいて製品を除外する方法について説明します。
author: ChristianRytt
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 371d98eefa482fc3e430f2f0977ddffb9dd0d30e
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645095"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a><span data-ttu-id="c8548-103">特定の製品ライフサイクル状態の製品を除外する</span><span class="sxs-lookup"><span data-stu-id="c8548-103">Exclude products that have specific product lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c8548-104">リリース済製品およびリリース済の製品バージョンには、**製品ライフサイクルの状態** フィールドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c8548-104">Released products and released product versions include a **Product lifecycle state** field.</span></span> <span data-ttu-id="c8548-105">このフィールドを使用すると、特にマスター プラン作成の際に含める製品を制御できます。</span><span class="sxs-lookup"><span data-stu-id="c8548-105">This field lets you control, among other things, which products are included during master planning.</span></span> <span data-ttu-id="c8548-106">**製品情報管理 \> 設定 \> 製品ライフサイクルの状態** に移動して、必要に応じてライフサイクルの状態を追加、削除、および編集できます。</span><span class="sxs-lookup"><span data-stu-id="c8548-106">You can add, remove, and edit lifecycle states as required by going to **Product information management \> Setup \> Product lifecycle state**.</span></span> <span data-ttu-id="c8548-107">製品ライフサイクルの各状態について、その状態を持つ製品がマスター プラン中に含まれる必要がある場合は、**計画に対して有効** オプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="c8548-107">For each product lifecycle state, set the **Is active for planning** option to *Yes* if products that have that state should be included during master planning.</span></span> <span data-ttu-id="c8548-108">このオプションを *いいえ* に設定すると、関連付けられている製品とバリアントは、部品表 (BOM) レベルのすべてのマスター プランと計算から除外されます。</span><span class="sxs-lookup"><span data-stu-id="c8548-108">When the option is set to *No*, the associated products and variants will be excluded from all master planning and all calculations at the bill of materials (BOM) level.</span></span>

<span data-ttu-id="c8548-109">**製品ライフサイクルの状態** フィールドが空白のままになっているリリースされた製品およびバリアントは、**計画に対して有効** オプションが *はい* に設定されている製品ライフサイクルの状態を持つものとして処理されます。</span><span class="sxs-lookup"><span data-stu-id="c8548-109">Released products and variants where the **Product lifecycle state** field is left blank are treated as though they have a product lifecycle state where the **Is active for planning** option is set to *Yes*.</span></span> <span data-ttu-id="c8548-110">つまり、マスター プラン作成の際に含まれます。</span><span class="sxs-lookup"><span data-stu-id="c8548-110">In other words, they will be included during master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="c8548-111">不要な入力候補を回避するために、**計画に対して有効** オプションが *いいえ* に設定されている製品ライフサイクル状態に、すべての古いリリース製品とバリアントを関連付けることを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c8548-111">To help avoid unnecessary supply suggestions, we strongly recommend that you associate all obsolete released products and variants with a product lifecycle state where the **Is active for planning** option is set to *No*.</span></span> <span data-ttu-id="c8548-112">この方法は、無駄を省くことができるため、再利用できない製品コンフィギュレーション バリアントを使用する場合に特に重要です。</span><span class="sxs-lookup"><span data-stu-id="c8548-112">This approach is especially important when you work with product configuration variants that aren't reusable, because it will help prevent waste.</span></span>

## <a name="related-resources"></a><span data-ttu-id="c8548-113">関連するリソース</span><span class="sxs-lookup"><span data-stu-id="c8548-113">Related resources</span></span>

<span data-ttu-id="c8548-114">製品ライフサイクルの状態の詳細については、[製品ライフサイクルの状態の概要](../../pim/product-lifecycle.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8548-114">For more information about product lifecycle states, see [Product lifecycle state overview](../../pim/product-lifecycle.md).</span></span>

<span data-ttu-id="c8548-115">製品ライフサイクルの状態を使用して、製品をマスター プランおよび BOM レベルの計算から製品を除外する手順の詳細については、[マスター プランから製品を除外する製品ライフサイクルの状態を作成](../../pim/tasks/exclude-products-master-planning.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8548-115">For detailed information that includes steps for using product lifecycle states to exclude products from master planning and BOM-level calculations, see [Create a product lifecycle state to exclude products from Master planning](../../pim/tasks/exclude-products-master-planning.md).</span></span>
