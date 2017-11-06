---
title: "分析コード ベースの製品コンフィギュレーション"
description: "分析コード ベースの製品コンフィギュレーションは、1 つの製品マスターと部品表から多くの製品バリアントを作成するための単純なソリューションを表します。"
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7b46adf0bef79eafb1dd4b0809965abdd3b4410c
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="dimension-based-product-configuration"></a><span data-ttu-id="6ad08-103">分析コード ベースの製品コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6ad08-103">Dimension-based product configuration</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6ad08-104">分析コード ベースの製品コンフィギュレーションは、1 つの製品マスターと部品表から多くの製品バリアントを作成するための単純なソリューションを表します。</span><span class="sxs-lookup"><span data-stu-id="6ad08-104">Dimension-based product configuration represents a simple solution for creating many product variants from a single product master and its bill of materials.</span></span>

<span data-ttu-id="6ad08-105">分析コード ベースの製品コンフィギュレーションは、3 つの組み込みの製品コンフィギュレーション テクノロジーの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="6ad08-105">Dimension-based product configuration is one of the three built-in product configuration technologies.</span></span> <span data-ttu-id="6ad08-106">他の 2 つのテクノロジは、定義済バリアントと制約ベースのコンフィギュレーションです。</span><span class="sxs-lookup"><span data-stu-id="6ad08-106">The two other technologies are predefined variants and constraint-based configuration.</span></span> <span data-ttu-id="6ad08-107">3 つのテクノロジはすべて開始点として製品マスターを使用し、ユーザーは 1 つの製品マスターに多くの製品バリアントを作成できます。</span><span class="sxs-lookup"><span data-stu-id="6ad08-107">All three technologies use a product master as the starting point and allow the user to create many product variants for one product master.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="6ad08-108">重要な概念</span><span class="sxs-lookup"><span data-stu-id="6ad08-108">Key concepts</span></span>
<span data-ttu-id="6ad08-109">分析コード ベースの製品コンフィギュレーションは次の重要な概念に基づいています。</span><span class="sxs-lookup"><span data-stu-id="6ad08-109">Dimension-based product configuration is based on the following key concepts:</span></span>

-   <span data-ttu-id="6ad08-110">製品マスター</span><span class="sxs-lookup"><span data-stu-id="6ad08-110">Product masters</span></span>
-   <span data-ttu-id="6ad08-111">製品分析コードのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6ad08-111">Configuration product dimension</span></span>
-   <span data-ttu-id="6ad08-112">コンフィギュレーション グループ</span><span class="sxs-lookup"><span data-stu-id="6ad08-112">Configuration groups</span></span>
-   <span data-ttu-id="6ad08-113">部品表 (BOM)</span><span class="sxs-lookup"><span data-stu-id="6ad08-113">Bill of materials (BOM)</span></span>
-   <span data-ttu-id="6ad08-114">コンフィギュレーション ルート</span><span class="sxs-lookup"><span data-stu-id="6ad08-114">Configuration route</span></span>
-   <span data-ttu-id="6ad08-115">コンフィギュレーション ルール</span><span class="sxs-lookup"><span data-stu-id="6ad08-115">Configuration rules</span></span>

### <a name="product-masters"></a><span data-ttu-id="6ad08-116">製品マスター</span><span class="sxs-lookup"><span data-stu-id="6ad08-116">Product masters</span></span>

<span data-ttu-id="6ad08-117">製品マスターは、製品コンフィギュレーション プロセスの開始点です。</span><span class="sxs-lookup"><span data-stu-id="6ad08-117">A product master is the starting point for any product configuration process.</span></span> <span data-ttu-id="6ad08-118">分析コード ベースの製品コンフィギュレーションでは、この特定のコンフィギュレーション テクノロジを使用した製品マスターとコンフィギュレーション製品分析コードを含む製品分析コード グループが必要です。</span><span class="sxs-lookup"><span data-stu-id="6ad08-118">For the dimension-based product configuration, you need a product master with this particular configuration technology and a product dimension group that includes the configuration product dimension.</span></span>

### <a name="configuration-product-dimension"></a><span data-ttu-id="6ad08-119">製品分析コードのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6ad08-119">Configuration product dimension</span></span>

<span data-ttu-id="6ad08-120">製品分析コードのコンフィギュレーションは、分析コード ベースのコンフィギュレーション テクノロジを使用した製品マスターの製品バリアントを識別するために使用します。</span><span class="sxs-lookup"><span data-stu-id="6ad08-120">The configuration product dimension is used to identify the product variants for a product master with the dimension-based configuration technology.</span></span> <span data-ttu-id="6ad08-121">コンフィギュレーション分析コード値はユーザーが入力し、個々の製品バリアントの識別に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="6ad08-121">The configuration dimension value is entered by the user and should help to identify the individual product variants.</span></span>

### <a name="configuration-groups"></a><span data-ttu-id="6ad08-122">コンフィギュレーション グループ</span><span class="sxs-lookup"><span data-stu-id="6ad08-122">Configuration groups</span></span>

<span data-ttu-id="6ad08-123">コンフィギュレーション グループは、中央レポジトリで定義され、すべての分析コード ベースの製品コンフィギュレーション モデルに使用できます。</span><span class="sxs-lookup"><span data-stu-id="6ad08-123">Configuration groups are defined in a central repository and can be used for all dimension-based product configuration models.</span></span> <span data-ttu-id="6ad08-124">コンフィギュレーション グループは、個々の BOM 明細行に関連付けられ、相互に排他的な明細行のグループをまとめます。</span><span class="sxs-lookup"><span data-stu-id="6ad08-124">Configuration groups are associated to the individual BOM lines and hold together a group of lines that are mutually exclusive.</span></span> <span data-ttu-id="6ad08-125">これは、1 つの製品バリアントに 1 つのグループの 1 つの明細行だけが選択できることを意味します。</span><span class="sxs-lookup"><span data-stu-id="6ad08-125">This means that only one line in a group can be selected for a single product variant.</span></span>

### <a name="bill-of-materials-bom"></a><span data-ttu-id="6ad08-126">部品表 (BOM)</span><span class="sxs-lookup"><span data-stu-id="6ad08-126">Bill of materials (BOM)</span></span>

<span data-ttu-id="6ad08-127">BOM は、分析コード ベースの製品コンフィギュレーションの構成要素を表します。</span><span class="sxs-lookup"><span data-stu-id="6ad08-127">The BOM represent the building blocks for a dimension-based product configuration.</span></span> <span data-ttu-id="6ad08-128">これには、製品バリアントに使用できるすべての異なる製品を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ad08-128">It must include all the different products that can be used in any product variant.</span></span> <span data-ttu-id="6ad08-129">BOM の各行は、コンフィギュレーション グループを参照できます。</span><span class="sxs-lookup"><span data-stu-id="6ad08-129">Each line in the BOM can reference a configuration group.</span></span> <span data-ttu-id="6ad08-130">明細行がコンフィギュレーション グループを参照しない場合は、すべての製品バリアントに含まれます。</span><span class="sxs-lookup"><span data-stu-id="6ad08-130">If a line doesn’t reference a configuration group, it will be included in all product variants.</span></span>

### <a name="configuration-route"></a><span data-ttu-id="6ad08-131">コンフィギュレーション ルート</span><span class="sxs-lookup"><span data-stu-id="6ad08-131">Configuration route</span></span>

<span data-ttu-id="6ad08-132">コンフィギュレーション ルートは、製品コンフィギュレーション プロセス中にユーザーが表示するときのコンフィギュレーション グループの順序を決定します。</span><span class="sxs-lookup"><span data-stu-id="6ad08-132">The configuration route determines the sequence of the configuration groups, as they will be displayed to the user during the product configuration process.</span></span>

### <a name="configuration-rules"></a><span data-ttu-id="6ad08-133">コンフィギュレーション ルール</span><span class="sxs-lookup"><span data-stu-id="6ad08-133">Configuration rules</span></span>

<span data-ttu-id="6ad08-134">コンフィギュレーション ルールは、ある BOM の 1 つのコンフィギュレーション グループに含まれている製品が、同じ BOM の別のコンフィギュレーション グループで他の製品を包含または排除することを確認するしくみを表します。</span><span class="sxs-lookup"><span data-stu-id="6ad08-134">The configuration rules represent a mechanism for ensuring that a product included in one configuration group in a BOM enforces either an inclusion or an exclusion of a product in a different configuration group in the same BOM.</span></span>

## <a name="product-modeling-process"></a><span data-ttu-id="6ad08-135">製品モデリング プロセス</span><span class="sxs-lookup"><span data-stu-id="6ad08-135">Product modeling process</span></span>
<span data-ttu-id="6ad08-136">分析コード ベースの製品の製品モデル作成のための正常な順序は、関連するコンフィギュレーション グループの定義で始まります。</span><span class="sxs-lookup"><span data-stu-id="6ad08-136">The natural sequence for building a product model for a dimension-based product starts with defining the relevant configuration groups.</span></span> <span data-ttu-id="6ad08-137">BOM で使用されるすべての製品が、製品モデルが作成された会社にリリース済みであることを確認することは重要です。</span><span class="sxs-lookup"><span data-stu-id="6ad08-137">It is important to ensure that all products which will be used in the BOM have been relased to the company that the product model is built for.</span></span> <span data-ttu-id="6ad08-138">ユーザーは、これらの構成要素を適切な場所で使用して、BOM を作成し、コンフィギュレーション グループを関連するすべての BOM 明細行に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="6ad08-138">With these building blocks in place, the user can create the BOM and assign configuration groups to all relevant BOM lines.</span></span> <span data-ttu-id="6ad08-139">BOM が完了すると、コンフィギュレーション ルートを、適切な順序でコンフィギュレーション グループの注文で定義できます。</span><span class="sxs-lookup"><span data-stu-id="6ad08-139">When the BOM is complete, a configuration route can be defined for ordering the configuration groups in the proper sequence.</span></span> <span data-ttu-id="6ad08-140">[![分析コード ベースの製品モデリングのプロセス](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png)一緒に使用する必要がある、または必要がない異なるコンフィギュレーション グループに製品が存在する場合、これらの製品の関係を適用するコンフィギュレーション ルールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="6ad08-140">[![Dimension-based product modeling process](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) If there are certain products from different configuration groups that either must or must not be used together, you can create configuration rules that will enforce these product relationships.</span></span> <span data-ttu-id="6ad08-141">BOM が BOM バージョンを介して分析コード ベースの製品マスターと結ばれ、両方とも承認され有効化されると、製品コンフィギュレーションを作成して、各コンフィギュレーションの名前を入力できます。</span><span class="sxs-lookup"><span data-stu-id="6ad08-141">After the BOM has been tied together with a dimension-based product master through a BOM version and both have been approved and activated, you can create product configurations and enter a name for each configuration.</span></span> <span data-ttu-id="6ad08-142">コンフィギュレーションは、トランザクションが生成される前に定義することができ、また特定のコンフィギュレーションの必要性が発生したときに定義することができます。</span><span class="sxs-lookup"><span data-stu-id="6ad08-142">The configurations can be defined before any transactions are generated or it can be done when the need for a certain configuration occurs.</span></span>

### <a name="suggested-use"></a><span data-ttu-id="6ad08-143">推奨される使用</span><span class="sxs-lookup"><span data-stu-id="6ad08-143">Suggested use</span></span>

<span data-ttu-id="6ad08-144">分析コード ベースのコンフィギュレーション テクノロジは、限られた可変性の製品に使用されます。また、標準的な製品分析コード サイズ、色、スタイル、およびコンフィギュレーションの組み合わせは、特定の製品バリアントを識別するのに不適切です。</span><span class="sxs-lookup"><span data-stu-id="6ad08-144">The dimension-based configuration technology is best used for products with limited variability and the combination of the standard product dimensions size, color, style, and configuration is unsuitable for identifying a specific product variant.</span></span> <span data-ttu-id="6ad08-145">例として、フレームの高さ、ホイールのサイズ、ブレーキ タイプ、およびさまざまなギヤを含む自転車が考えられます。</span><span class="sxs-lookup"><span data-stu-id="6ad08-145">An example could be bicycle with frame height, wheel size, brake types, and different gears.</span></span>

### <a name="next-step"></a><span data-ttu-id="6ad08-146">次のステップ</span><span class="sxs-lookup"><span data-stu-id="6ad08-146">Next step</span></span> 

<span data-ttu-id="6ad08-147">以下の 8 つのタスク ガイドは、実行する必要のある順番で一覧表示されています。</span><span class="sxs-lookup"><span data-stu-id="6ad08-147">The following eight task guides are listed in the order in which you should complete them.</span></span> 

1.  [<span data-ttu-id="6ad08-148">分析コードベースの製品マスターの作成 (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="6ad08-148">Create a dimension-based product master (Task guide)</span></span>](tasks/create-dimension-based-product-master.md)
2.  [<span data-ttu-id="6ad08-149">分析コードベースの製品マスターのリリース (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="6ad08-149">Release a dimension-based product master (Task guide)</span></span>](tasks/release-dimension-based-product-master.md)
3.  [<span data-ttu-id="6ad08-150">リリース済み製品マスターの基本設定の完了 (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="6ad08-150">Complete basic setup of a released product master (Task guide)</span></span>](tasks/complete-basic-setup-released-product-master.md)
4.  [<span data-ttu-id="6ad08-151">コンフィギュレーション グループの定義 (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="6ad08-151">Define configuration groups (Task guide)</span></span>](tasks/define-configuration-groups.md)
5.  [<span data-ttu-id="6ad08-152">分析コード ベースの製品マスターの部品表の作成 (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="6ad08-152">Create a bill of materials for a dimension-based product master (Task guide)</span></span>](tasks/create-bill-materials-dimension-based-product-master.md)
6.  [<span data-ttu-id="6ad08-153">コンフィギュレーション工順の定義 (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="6ad08-153">Define configuration routes (Task guide)</span></span>](tasks/define-configuration-route.md)
7.  [<span data-ttu-id="6ad08-154">コンフィギュレーション ルールの作成 (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="6ad08-154">Create configuration rules (Task guide)</span></span>](tasks/create-configuration-rules.md)
8.  [<span data-ttu-id="6ad08-155">分析コードベースのコンフィギュレーションの作成 (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="6ad08-155">Create dimension-based configurations (Task guide)</span></span>](tasks/create-dimension-based-configurations.md)

