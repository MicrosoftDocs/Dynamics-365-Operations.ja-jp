---
title: "製品カテゴリの管理"
description: "このトピックでは、販売促進マネージャーが小売製品カテゴリを使用して、小売製品階層とリリースされた製品の詳細な関係を管理する方法について説明します。"
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 4b7ef962b777a31e1da238a8ec1be9a42ec5bb5f
ms.contentlocale: ja-jp
ms.lasthandoff: 03/13/2018

---


# <a name="enhanced-product-and-category-management"></a><span data-ttu-id="60eee-103">拡張された製品とカテゴリの管理</span><span class="sxs-lookup"><span data-stu-id="60eee-103">Enhanced product and category management</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="60eee-104">このトピックでは、Dynamics 365 for Retail の小売製品カテゴリと製品を管理するための強化された方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="60eee-104">This topic describes an enhanced way to manage Retail product categories and products in Dynamics 365 for Retail.</span></span> <span data-ttu-id="60eee-105">これらの拡張機能で、販売促進マネージャーは小売製品階層、およびリリース済製品の詳細の間の、製品プロパティ製品の共通構造を表示できます。</span><span class="sxs-lookup"><span data-stu-id="60eee-105">These enhancements let merchandising managers view a common structure of product properties between Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="60eee-106">小売製品カテゴリの管理に関する詳細については、[カテゴリと製品の管理] ワークスペースから [小売製品カテゴリ] へ移動し、[小売製品カテゴリ] ページの拡張構造に注意してください。</span><span class="sxs-lookup"><span data-stu-id="60eee-106">To learn more about managing Retail product categories, go to **Retail product hierarchy** from the **Category and product management** workspace, and note the enhanced structure of the **Retail product category** page.</span></span>

![カテゴリと製品の管理ワークスペース](media/LaunchRetailProductHierarchy.png)

<span data-ttu-id="60eee-108">以前のバージョンでは、製品のプロパティは適用性の範囲に基づいて [基本的な製品プロパティ] と [小売製品プロパティ] に分割されていました。</span><span class="sxs-lookup"><span data-stu-id="60eee-108">In previous versions, product properties were divided into **Basic product properties** and **Retail product properties**, based on the scope of their applicability.</span></span> <span data-ttu-id="60eee-109">[小売製品プロパティ] は適用の範囲で*グローバル*であり、これは特定の [小売製品プロパティ] について、すべての法人で同じ値が共有されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="60eee-109">**Retail product properties** were *global* by scope of applicability, which means that for a given **Retail product property**, the same value is shared across all legal entities.</span></span> <span data-ttu-id="60eee-110">[基本的な製品プロパティ] は*法人固有*です。</span><span class="sxs-lookup"><span data-stu-id="60eee-110">**Basic product properties** are *legal entity specific*.</span></span> <span data-ttu-id="60eee-111">つまり、特定の [基本的な製品プロパティ] では、個々の業務要件に基づいて、法人間で値が異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="60eee-111">In other words, for a given **Basic product property** the value can differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="60eee-112">拡張された小売製品カテゴリ構造では、リリースされた製品の詳細フォーム構造を反映するために、グループ内の適用性に基づいて製品プロパティが論理的に分離されます。</span><span class="sxs-lookup"><span data-stu-id="60eee-112">In the enhanced Retail product category structure, product properties are logically separated based on their applicability within a group, to reflect the released product details form structure.</span></span>

![適用範囲に基づいたフィールドのグループ化](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="60eee-114">法人特定のプロパティをすべての法人で管理するか、特定の法人用に管理するかのどちらかに切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="60eee-114">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="60eee-115">そのためには、[すべての法人用に表示/編集] または [特定の法人用に表示/編集] のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="60eee-115">To do this, select either **View/Edit for all legal entities** or **View/Edit for a specific legal entity**.</span></span>

![個人とすべての法人の表示の切り替え](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![個人とすべての法人の表示の切り替え](media/ToggleToEditForAllLegalEntities.PNG)  

<span data-ttu-id="60eee-118">以前のバージョンと比較して、新しい小売製品カテゴリ構造では、販売促進マネージャーは、個々のカテゴリ レベルで追加の製品プロパティ セットの既定値を定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="60eee-118">Compared to previous versions, in the new Retail product category structure a merchandising manager can also define default values for an additional set of product properties at an individual category level.</span></span> <span data-ttu-id="60eee-119">製品の作成時には、これらのデフォルトの製品プロパティ値は、小売製品階層からの個々のカテゴリとの関連性に基づいて、製品に継承されます。</span><span class="sxs-lookup"><span data-stu-id="60eee-119">At the time of product creation, these default product property values are inherited by a product, based on their association with an individual category from Retail product hierarchy.</span></span> <span data-ttu-id="60eee-120">これらの継承された製品プロパティは、個々の業務要件を満たすために、製品ごとに変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="60eee-120">These inherited product properties can also be modified for each product, to meet individual business requirements.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="60eee-121">プロパティを選択して Retail 製品カテゴリ フォームから製品を更新する</span><span class="sxs-lookup"><span data-stu-id="60eee-121">Select properties to update products from the Retail product category form</span></span> 
 
<span data-ttu-id="60eee-122">この新しい拡張された製品プロパティ構造を使用して、更新された製品プロパティが関連付けられた製品にプッシュされる必要があるかを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="60eee-122">You can use this new enhanced structure for product properties to select which updated product properties must be pushed to associated products.</span></span> 

![製品更新の新しい拡張ビュー](media/NewUpdateProductsEnhancedView.PNG) 

<span data-ttu-id="60eee-124">販売促進マネージャーは、個々の業務要件を満たすために、各製品のこれらの継承された製品プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="60eee-124">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>


