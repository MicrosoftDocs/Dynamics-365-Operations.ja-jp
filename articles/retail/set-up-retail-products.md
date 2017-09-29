---
title: "小売製品の設定"
description: "この記事では、Microsoft Dynamics 365 for Retail での小売製品の設定方法について説明します。"
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 85b794bb1a1a7a4e9b0e811d90408ed8872a6f0a
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---

# <a name="set-up-retail-products"></a><span data-ttu-id="86639-103">小売製品の設定</span><span class="sxs-lookup"><span data-stu-id="86639-103">Set up retail products</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="86639-104">この記事では、Microsoft Dynamics 365 for Retail での小売製品の設定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="86639-104">This article describes how to set up retail products in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="86639-105">小売チャネルで製品を再販するには、Dynamics 365 for Retail で製品の作成とコンフィギュレーションを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="86639-105">Before you can offer products for resale in your retail channels, you must create and configure the products in Dynamics 365 for Retail.</span></span> <span data-ttu-id="86639-106">小売は、Dynamics 365 for Retail の製品の機能を使用して、製品マスターで組織全体の製品を作成します。</span><span class="sxs-lookup"><span data-stu-id="86639-106">Retail uses the product features in Dynamics 365 for Retail to create organization-wide products in the product master.</span></span> <span data-ttu-id="86639-107">製品の作成、製品のプロパティおよび属性の定義、および小売カテゴリ階層への製品の割り当てを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="86639-107">You can create the products, define the product properties and attributes, and assign the products to retail category hierarchies.</span></span> <span data-ttu-id="86639-108">製品を小売チャンネルで利用可能にして有効な品揃えに追加するには、製品を利用可能にする法人に製品をリリースする必要があります。</span><span class="sxs-lookup"><span data-stu-id="86639-108">To make the products available to your retail channels and add them to an active assortment, you must release the products to the legal entities where they are available.</span></span> <span data-ttu-id="86639-109">小売チャンネルを使用して販売する製品を設定するには、次の作業を行います。</span><span class="sxs-lookup"><span data-stu-id="86639-109">To set up the products that you sell by using retail channels, complete the following tasks.</span></span>

1.  <span data-ttu-id="86639-110">小売製品階層を定義します。</span><span class="sxs-lookup"><span data-stu-id="86639-110">Define a retail product hierarchy.</span></span> <span data-ttu-id="86639-111">Dynamics 365 for Retail のカテゴリ階層機能を使用することで、小売カテゴリ階層を定義し、小売チャンネルに配分する製品をグループ化および分類できます。</span><span class="sxs-lookup"><span data-stu-id="86639-111">By using the category hierarchy features in Dynamics 365 for Retail, you can define retail category hierarchies to group and categorize the products that you distribute to your retail channels.</span></span> <span data-ttu-id="86639-112">ユーザー定義属性とシステム属性をカテゴリ レベルで定義できます。</span><span class="sxs-lookup"><span data-stu-id="86639-112">User-defined and system attributes can be defined at the category level.</span></span> <span data-ttu-id="86639-113">その後、カテゴリに割り当てられているすべての製品は、これらの属性を継承します。</span><span class="sxs-lookup"><span data-stu-id="86639-113">Then, all products that are assigned to the category inherit those attributes.</span></span> <span data-ttu-id="86639-114">複数のカテゴリ階層を定義したり、各製品を複数の階層に割り当てたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="86639-114">Multiple category hierarchies can be defined, and each product can be assigned to multiple hierarchies.</span></span> <span data-ttu-id="86639-115">ただし、1 つの階層では、各製品を 1 つのカテゴリにのみ割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="86639-115">However, in a single hierarchy, each product can be assigned to only one category.</span></span>
2.  <span data-ttu-id="86639-116">製品および製品バリアントを製品マスター追加します。</span><span class="sxs-lookup"><span data-stu-id="86639-116">Add products and product variants to the product master.</span></span> <span data-ttu-id="86639-117">製品マスターに追加される製品は、製品の全体的な一覧を表します。</span><span class="sxs-lookup"><span data-stu-id="86639-117">Products that are added to the product master represent a global list of products.</span></span> <span data-ttu-id="86639-118">製品を 1 つずつ手動で追加したり、仕入先から製品データをインポートしたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="86639-118">You can add products manually, one at a time, or you can import product data from your vendors.</span></span>
3.  <span data-ttu-id="86639-119">法人への製品のリリース</span><span class="sxs-lookup"><span data-stu-id="86639-119">Release the products to legal entities.</span></span> <span data-ttu-id="86639-120">法人にリリースされている製品のみを小売チャンネルで利用可能にすることができます。</span><span class="sxs-lookup"><span data-stu-id="86639-120">Only products that have been released to legal entities can be made available to your retail channels.</span></span> <span data-ttu-id="86639-121">初めて製品を定義する場合、製品を組織全体のレベルで定義します。</span><span class="sxs-lookup"><span data-stu-id="86639-121">When you first define a product, you define it on an organization-wide level.</span></span> <span data-ttu-id="86639-122">次に、製品をリリースする 1 つ以上の法人を選択できます。</span><span class="sxs-lookup"><span data-stu-id="86639-122">You can then select one or more legal entities to release the product to.</span></span> <span data-ttu-id="86639-123">その後、製品が組織全体の複数の小売チャンネルで利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="86639-123">The product then becomes available to multiple retail channels across your organization.</span></span> <span data-ttu-id="86639-124">この機能を使用して、1 回製品を作成し、1 つの場所で製品の属性およびプロパティを更新し、製品が使用可能な小売チャンネルに組織全体の製品を配分できます。</span><span class="sxs-lookup"><span data-stu-id="86639-124">You can use this functionality to create a product one time, add and update product attributes and properties in one place, and then distribute the product across your organization, to the retail channels where it's available.</span></span>
4.  <span data-ttu-id="86639-125">製品を品揃えに追加します。</span><span class="sxs-lookup"><span data-stu-id="86639-125">Add products to assortments.</span></span> <span data-ttu-id="86639-126">品揃えは、小売チャンネルで提供する製品の集まりを表します。</span><span class="sxs-lookup"><span data-stu-id="86639-126">An assortment represents a collection of products that you offer in your retail channels.</span></span> <span data-ttu-id="86639-127">1 つまたは複数の品揃えを定義し、各製品を 1 つまたは複数の品揃えに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="86639-127">You can define one or more assortments, and each product can be assigned to one or more assortments.</span></span> <span data-ttu-id="86639-128">製品を小売チャンネルに割り当てるには、品揃えをそれらの小売チャンネルに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="86639-128">To assign products to retail channels, you assign the assortments to those retail channels.</span></span> <span data-ttu-id="86639-129">品揃えを作成すると、法人にまだにリリースされていない製品を追加できます。</span><span class="sxs-lookup"><span data-stu-id="86639-129">When you create an assortment, you can add products that haven't yet been released to a legal entity.</span></span> <span data-ttu-id="86639-130">ただし、製品を小売チャンネルで利用可能にする前に、それらの製品を法人にリリースする必要があります。</span><span class="sxs-lookup"><span data-stu-id="86639-130">However, you must release the products to a legal entity before those products can be made available to the retail channels.</span></span>
5.  <span data-ttu-id="86639-131">ナビゲーション階層に製品を追加します。</span><span class="sxs-lookup"><span data-stu-id="86639-131">Add products to navigation hierarchies.</span></span> <span data-ttu-id="86639-132">製品がオンラインまたは販売時点管理 (POS) で閲覧できるようにするためには、[小売ナビゲーション階層] に分類する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86639-132">Before products can be browsed online or in point of sale (POS), they must be categorized in a Retail navigation hierarchy.</span></span>
6.  <span data-ttu-id="86639-133">製品をカタログに追加します。</span><span class="sxs-lookup"><span data-stu-id="86639-133">Add products to catalogs.</span></span> <span data-ttu-id="86639-134">このステップは POS では省略可能ですが、オンライン ストアでは製品が少なくとも 1 つのカタログに含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="86639-134">Although this step is optional for POS, online stores require that products be included in at least one catalog.</span></span>





