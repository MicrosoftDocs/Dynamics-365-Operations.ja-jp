---
title: "小売階層"
description: "この記事は、Microsoft Dynamics 365 for Retail の小売階層について説明します。"
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
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 817696566473bc5f31a7ff11c04291351dfd4764
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="retail-hierarchies"></a><span data-ttu-id="cf52d-103">小売階層</span><span class="sxs-lookup"><span data-stu-id="cf52d-103">Retail hierarchies</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="cf52d-104">この記事は、Microsoft Dynamics 365 for Retail の小売階層について説明します。</span><span class="sxs-lookup"><span data-stu-id="cf52d-104">This article describes retail hierarchies in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="cf52d-105">小売カテゴリ階層を作成して、小売チャンネルを使用して販売する製品を整理することができます。</span><span class="sxs-lookup"><span data-stu-id="cf52d-105">You can create a retail category hierarchy to organize the products that you sell through your retail channels.</span></span> <span data-ttu-id="cf52d-106">小売製品階層を使用して、製品を分類またはグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="cf52d-106">You can use retail product hierarchies to categorize or group products.</span></span> <span data-ttu-id="cf52d-107">その後、これらの製品を使用して、製品の品揃えと顧客ロイヤルティ プログラムを作成できます。</span><span class="sxs-lookup"><span data-stu-id="cf52d-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="cf52d-108">また、製品の属性またはプロパティの割り当て、価格決定構造の割り当て、製品プロモーションへの製品の挿入、およびレポートでの製品の使用を行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="cf52d-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="cf52d-109">1 つの小売カテゴリ階層を作成して組織のすべての製品およびカテゴリを表し、複数の目的にその小売カテゴリ階層を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="cf52d-109">You can create one retail category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="cf52d-110">また、製品のプロモーションなどの特殊な目的に複数の小売カテゴリ階層を作成できます。</span><span class="sxs-lookup"><span data-stu-id="cf52d-110">Alternatively, you can create multiple retail category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="cf52d-111">小売製品階層を作成する際に、カテゴリ階層の目的を識別するためにカテゴリ階層タイプを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf52d-111">When you create a retail product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="cf52d-112">たとえば、**小売のナビゲーション階層**タイプが割り当てられている製品階層のみが、製品をカテゴリごとにオンラインで、または販売時点管理 (POS) で表示する場合に参照されます。</span><span class="sxs-lookup"><span data-stu-id="cf52d-112">For example, only product hierarchies that are assigned the **Retail navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="retail-hierarchy-types"></a><span data-ttu-id="cf52d-113">小売階層のタイプ</span><span class="sxs-lookup"><span data-stu-id="cf52d-113">Retail hierarchy types</span></span>
<span data-ttu-id="cf52d-114">次の表に、使用できる小売カテゴリ階層のタイプと各タイプの一般的な目的を示します。</span><span class="sxs-lookup"><span data-stu-id="cf52d-114">The following table lists the types of retail category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="cf52d-115">カテゴリ階層タイプ</span><span class="sxs-lookup"><span data-stu-id="cf52d-115">Category hierarchy type</span></span>       | <span data-ttu-id="cf52d-116">目的</span><span class="sxs-lookup"><span data-stu-id="cf52d-116">Purpose</span></span>                                                                                                                                                                                                                                                                                                            |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf52d-117">小売製品階層</span><span class="sxs-lookup"><span data-stu-id="cf52d-117">Retail product hierarchy</span></span>      | <span data-ttu-id="cf52d-118">組織の全体的な製品階層を定義するには、この階層タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="cf52d-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="cf52d-119">販売促進、価格決定とプロモーション、および品揃え計画にこの階層タイプを使用できます。</span><span class="sxs-lookup"><span data-stu-id="cf52d-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="cf52d-120">1 つの小売階層にのみこの製品グループ タイプを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="cf52d-120">Only one retail product hierarchy can be assigned this hierarchy type.</span></span>                                       |
| <span data-ttu-id="cf52d-121">補助小売階層</span><span class="sxs-lookup"><span data-stu-id="cf52d-121">Supplemental retail hierarchy</span></span> | <span data-ttu-id="cf52d-122">作成する追加の小売カテゴリ階層の場合には、このタイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="cf52d-122">Use this hierarchy type for any additional retail category hierarchies that you want to create.</span></span> <span data-ttu-id="cf52d-123">たとえば、春に水着のプロモーションがあります。</span><span class="sxs-lookup"><span data-stu-id="cf52d-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="cf52d-124">したがって、別のカテゴリ階層に水着製品を追加し、さまざまな製品カテゴリにプロモーション用の価格決定を適用します。</span><span class="sxs-lookup"><span data-stu-id="cf52d-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="cf52d-125">小売ナビゲーション階層</span><span class="sxs-lookup"><span data-stu-id="cf52d-125">Retail navigation hierarchy</span></span>   | <span data-ttu-id="cf52d-126">この階層タイプを使用すると、製品をグループ化してカテゴリに整理し、製品がオンラインまたは POS で閲覧できるようになります。</span><span class="sxs-lookup"><span data-stu-id="cf52d-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span>                                                                                                                                                                                       |

<span data-ttu-id="cf52d-127">小売カテゴリ階層を使用して製品を構造化することで、製品の属性およびプロパティをカテゴリ レベルで設定および管理できます。</span><span class="sxs-lookup"><span data-stu-id="cf52d-127">By using a retail category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="cf52d-128">これらの属性およびプロパティには、製品分析コードおよび POS の設定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="cf52d-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="cf52d-129">そのカテゴリに割り当てる製品は、定義するプロパティと属性を自動的に継承します。</span><span class="sxs-lookup"><span data-stu-id="cf52d-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="cf52d-130">また、選択したカテゴリの複数の製品に、製品のプロパティ設定を同時にコピーできます。</span><span class="sxs-lookup"><span data-stu-id="cf52d-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>




