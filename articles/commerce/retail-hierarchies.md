---
title: コマース階層
description: この記事は、Dynamics 365 Commerce の階層について説明します。
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: OMHierarchyManager, EcoResCategoryHierarchyFactbox
audience: Application User
ms.reviewer: josaw
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 94b391ab5028f76debb75d25ac9469e25361cb12
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979619"
---
# <a name="commerce-hierarchies"></a><span data-ttu-id="13be9-103">コマース階層</span><span class="sxs-lookup"><span data-stu-id="13be9-103">Commerce hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="13be9-104">この記事は、Dynamics 365 Commerce の階層について説明します。</span><span class="sxs-lookup"><span data-stu-id="13be9-104">This article describes hierarchies in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="13be9-105">カテゴリ階層を作成して、チャンネルを使用して販売する製品を整理することができます。</span><span class="sxs-lookup"><span data-stu-id="13be9-105">You can create a category hierarchy to organize the products that you sell through your channels.</span></span> <span data-ttu-id="13be9-106">製品階層を使用して、製品を分類またはグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="13be9-106">You can use product hierarchies to categorize or group products.</span></span> <span data-ttu-id="13be9-107">その後、これらの製品を使用して、製品の品揃えと顧客ロイヤルティ プログラムを作成できます。</span><span class="sxs-lookup"><span data-stu-id="13be9-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="13be9-108">また、製品の属性またはプロパティの割り当て、価格決定構造の割り当て、製品プロモーションへの製品の挿入、およびレポートでの製品の使用を行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="13be9-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="13be9-109">1 つのカテゴリ階層を作成して組織のすべての製品およびカテゴリを表し、複数の目的にそのカテゴリ階層を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="13be9-109">You can create one category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="13be9-110">また、製品のプロモーションなどの特殊な目的に複数のカテゴリ階層を作成できます。</span><span class="sxs-lookup"><span data-stu-id="13be9-110">Alternatively, you can create multiple category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="13be9-111">製品階層を作成する際に、カテゴリ階層の目的を識別するためにカテゴリ階層タイプを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="13be9-111">When you create a product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="13be9-112">たとえば、**コマースのナビゲーション階層** タイプが割り当てられている製品階層のみが、製品をカテゴリごとにオンラインで、または販売時点管理 (POS) で表示する場合に参照されます。</span><span class="sxs-lookup"><span data-stu-id="13be9-112">For example, only product hierarchies that are assigned the **Commerce navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="hierarchy-types"></a><span data-ttu-id="13be9-113">階層タイプ</span><span class="sxs-lookup"><span data-stu-id="13be9-113">Hierarchy types</span></span>

<span data-ttu-id="13be9-114">次の表に、使用できるカテゴリ階層のタイプと各タイプの一般的な目的を示します。</span><span class="sxs-lookup"><span data-stu-id="13be9-114">The following table lists the types of category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="13be9-115">カテゴリ階層タイプ</span><span class="sxs-lookup"><span data-stu-id="13be9-115">Category hierarchy type</span></span>       | <span data-ttu-id="13be9-116">目的</span><span class="sxs-lookup"><span data-stu-id="13be9-116">Purpose</span></span> |
|-------------------------------|---------|
| <span data-ttu-id="13be9-117">製品階層</span><span class="sxs-lookup"><span data-stu-id="13be9-117">Product hierarchy</span></span>      | <span data-ttu-id="13be9-118">組織の全体的な製品階層を定義するには、この階層タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="13be9-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="13be9-119">販売促進、価格決定とプロモーション、および品揃え計画にこの階層タイプを使用できます。</span><span class="sxs-lookup"><span data-stu-id="13be9-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="13be9-120">1 つの階層にのみこの製品グループ タイプを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="13be9-120">Only one product hierarchy can be assigned this hierarchy type.</span></span> |
| <span data-ttu-id="13be9-121">補助階層</span><span class="sxs-lookup"><span data-stu-id="13be9-121">Supplemental hierarchy</span></span> | <span data-ttu-id="13be9-122">作成する追加のカテゴリ階層の場合には、このタイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="13be9-122">Use this hierarchy type for any additional category hierarchies that you want to create.</span></span> <span data-ttu-id="13be9-123">たとえば、春に水着のプロモーションがあります。</span><span class="sxs-lookup"><span data-stu-id="13be9-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="13be9-124">したがって、別のカテゴリ階層に水着製品を追加し、さまざまな製品カテゴリにプロモーション用の価格決定を適用します。</span><span class="sxs-lookup"><span data-stu-id="13be9-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="13be9-125">ナビゲーション階層</span><span class="sxs-lookup"><span data-stu-id="13be9-125">Navigation hierarchy</span></span>   | <span data-ttu-id="13be9-126">この階層タイプを使用すると、製品をグループ化してカテゴリに整理し、製品がオンラインまたは POS で閲覧できるようになります。</span><span class="sxs-lookup"><span data-stu-id="13be9-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span> |

<span data-ttu-id="13be9-127">カテゴリ階層を使用して製品を構造化することで、製品の属性およびプロパティをカテゴリ レベルで設定および管理できます。</span><span class="sxs-lookup"><span data-stu-id="13be9-127">By using a category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="13be9-128">これらの属性およびプロパティには、製品分析コードおよび POS の設定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="13be9-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="13be9-129">そのカテゴリに割り当てる製品は、定義するプロパティと属性を自動的に継承します。</span><span class="sxs-lookup"><span data-stu-id="13be9-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="13be9-130">また、選択したカテゴリの複数の製品に、製品のプロパティ設定を同時にコピーできます。</span><span class="sxs-lookup"><span data-stu-id="13be9-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>
