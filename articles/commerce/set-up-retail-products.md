---
title: 小売製品の設定
description: この記事では、Dynamics 365 Commerce での小売製品の設定方法について説明します。
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailProductAndCategoryWorkspace, EcoResProductDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e8f624f5feb8ee8f641a9b35ae31bdfe38e5e0ce
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023182"
---
# <a name="set-up-retail-products"></a><span data-ttu-id="3b7ea-103">小売製品の設定</span><span class="sxs-lookup"><span data-stu-id="3b7ea-103">Set up retail products</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3b7ea-104">この記事では、Dynamics 365 Commerce での製品の設定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3b7ea-104">This article describes how to set up products in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3b7ea-105">コマース チャネルで製品を再販するには、製品の作成とコンフィギュレーションを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b7ea-105">Before you can offer products for resale in your commerce channels, you must create and configure the products.</span></span> <span data-ttu-id="3b7ea-106">コマースでは、製品マスターで組織全体の製品が作成されます。</span><span class="sxs-lookup"><span data-stu-id="3b7ea-106">Commerce creates organization-wide products in the product master.</span></span> <span data-ttu-id="3b7ea-107">製品を作成し、製品のプロパティと属性を定義し、コマース カテゴリ階層に製品を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="3b7ea-107">You can create the products, define the product properties and attributes, and assign the products to commerce category hierarchies.</span></span> <span data-ttu-id="3b7ea-108">製品をコマース チャネルで利用可能にして有効な品揃えに追加するには、製品を利用可能にする法人に製品をリリースする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b7ea-108">To make the products available to your channels and add them to an active assortment, you must release the products to the legal entities where they are available.</span></span> <span data-ttu-id="3b7ea-109">コマース チャネルを使用して販売する製品を設定するには、次の作業を行います。</span><span class="sxs-lookup"><span data-stu-id="3b7ea-109">To set up the products that you sell by using channels, complete the following tasks.</span></span>

1. <span data-ttu-id="3b7ea-110">**製品階層を定義します。**</span><span class="sxs-lookup"><span data-stu-id="3b7ea-110">**Define a product hierarchy.**</span></span> <span data-ttu-id="3b7ea-111">コマースのカテゴリ階層機能を使用することで、カテゴリ階層を定義し、チャネルに配分する製品をグループ化および分類できます。</span><span class="sxs-lookup"><span data-stu-id="3b7ea-111">By using the category hierarchy features in Commerce, you can define category hierarchies to group and categorize the products that you distribute to your channels.</span></span> <span data-ttu-id="3b7ea-112">ユーザー定義属性とシステム属性をカテゴリ レベルで定義できます。</span><span class="sxs-lookup"><span data-stu-id="3b7ea-112">User-defined and system attributes can be defined at the category level.</span></span> <span data-ttu-id="3b7ea-113">その後、カテゴリに割り当てられているすべての製品は、これらの属性を継承します。</span><span class="sxs-lookup"><span data-stu-id="3b7ea-113">Then, all products that are assigned to the category inherit those attributes.</span></span> <span data-ttu-id="3b7ea-114">複数のカテゴリ階層を定義したり、各製品を複数の階層に割り当てたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="3b7ea-114">Multiple category hierarchies can be defined, and each product can be assigned to multiple hierarchies.</span></span> <span data-ttu-id="3b7ea-115">ただし、1 つの階層では、各製品を 1 つのカテゴリにのみ割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="3b7ea-115">However, in a single hierarchy, each product can be assigned to only one category.</span></span>
2. <span data-ttu-id="3b7ea-116">**製品および製品バリアントを製品マスター追加します。**</span><span class="sxs-lookup"><span data-stu-id="3b7ea-116">**Add products and product variants to the product master.**</span></span> <span data-ttu-id="3b7ea-117">製品マスターに追加される製品は、製品の全体的な一覧を表します。</span><span class="sxs-lookup"><span data-stu-id="3b7ea-117">Products that are added to the product master represent a global list of products.</span></span> <span data-ttu-id="3b7ea-118">製品を 1 つずつ手動で追加したり、仕入先から製品データをインポートしたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="3b7ea-118">You can add products manually, one at a time, or you can import product data from your vendors.</span></span>
3. <span data-ttu-id="3b7ea-119">**法人への製品のリリース**</span><span class="sxs-lookup"><span data-stu-id="3b7ea-119">**Release the products to legal entities.**</span></span> <span data-ttu-id="3b7ea-120">法人にリリースされた製品のみをチャネルで利用可能にすることができます。</span><span class="sxs-lookup"><span data-stu-id="3b7ea-120">Only products that have been released to legal entities can be made available to your channels.</span></span> <span data-ttu-id="3b7ea-121">初めて製品を定義する場合、製品を組織全体のレベルで定義します。</span><span class="sxs-lookup"><span data-stu-id="3b7ea-121">When you first define a product, you define it on an organization-wide level.</span></span> <span data-ttu-id="3b7ea-122">次に、製品をリリースする 1 つ以上の法人を選択できます。</span><span class="sxs-lookup"><span data-stu-id="3b7ea-122">You can then select one or more legal entities to release the product to.</span></span> <span data-ttu-id="3b7ea-123">その後、製品が組織全体の複数のチャネルで利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="3b7ea-123">The product then becomes available to multiple channels across your organization.</span></span> <span data-ttu-id="3b7ea-124">この機能を使用して、1 回製品を作成し、1 つの場所で製品の属性およびプロパティを更新し、製品が使用可能なチャネルに組織全体の製品を配分できます。</span><span class="sxs-lookup"><span data-stu-id="3b7ea-124">You can use this functionality to create a product one time, add and update product attributes and properties in one place, and then distribute the product across your organization, to the channels where it's available.</span></span>
4. <span data-ttu-id="3b7ea-125">**製品を品揃えに追加します。**</span><span class="sxs-lookup"><span data-stu-id="3b7ea-125">**Add products to assortments.**</span></span> <span data-ttu-id="3b7ea-126">品揃えは、チャネルで提供する製品の集まりを表します。</span><span class="sxs-lookup"><span data-stu-id="3b7ea-126">An assortment represents a collection of products that you offer in your channels.</span></span> <span data-ttu-id="3b7ea-127">1 つまたは複数の品揃えを定義し、各製品を 1 つまたは複数の品揃えに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="3b7ea-127">You can define one or more assortments, and each product can be assigned to one or more assortments.</span></span> <span data-ttu-id="3b7ea-128">製品をチャネルに割り当てるには、品揃えをそれらのチャネルに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="3b7ea-128">To assign products to channels, you assign the assortments to those channels.</span></span> <span data-ttu-id="3b7ea-129">品揃えを作成すると、法人にまだにリリースされていない製品を追加できます。</span><span class="sxs-lookup"><span data-stu-id="3b7ea-129">When you create an assortment, you can add products that haven't yet been released to a legal entity.</span></span> <span data-ttu-id="3b7ea-130">ただし、製品をチャネルで利用可能にする前に、それらの製品を法人にリリースする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b7ea-130">However, you must release the products to a legal entity before those products can be made available to the channels.</span></span>
5. <span data-ttu-id="3b7ea-131">**ナビゲーション階層に製品を追加します。**</span><span class="sxs-lookup"><span data-stu-id="3b7ea-131">**Add products to navigation hierarchies.**</span></span> <span data-ttu-id="3b7ea-132">製品がオンラインまたは販売時点管理 (POS) で閲覧できるようにするためには、コマース ナビゲーション階層に分類する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b7ea-132">Before products can be browsed online or in point of sale (POS), they must be categorized in a Commerce navigation hierarchy.</span></span>
6. <span data-ttu-id="3b7ea-133">**製品をカタログに追加します。**</span><span class="sxs-lookup"><span data-stu-id="3b7ea-133">**Add products to catalogs.**</span></span> <span data-ttu-id="3b7ea-134">このステップは POS では省略可能ですが、オンライン ストアでは製品が少なくとも 1 つのカタログに含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b7ea-134">Although this step is optional for POS, online stores require that products be included in at least one catalog.</span></span>
