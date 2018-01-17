---
title: "製品カテゴリの管理と作成"
description: "このトピックでは、Retail 製品カテゴリの管理エクスペリエンスに対する拡張機能について説明します。 これらの拡張機能で、販売促進マネージャーは Retail 製品階層とリリース済製品の詳細との間に相関関係を持てます。"
author: ashishmsft
manager: AnnBe
ms.date: 09/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Retail
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 98250062892e0c5f665616dc3944181a3ff8599a
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="product-category-management-and-creation"></a><span data-ttu-id="a6ea0-104">製品カテゴリの管理と作成</span><span class="sxs-lookup"><span data-stu-id="a6ea0-104">Product category management and creation</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="a6ea0-105">Retail 製品カテゴリの管理エクスペリエンスに対する拡張機能で、販売促進マネージャーは Retail 製品階層とリリース済製品の詳細との間に相関関係を持てます。</span><span class="sxs-lookup"><span data-stu-id="a6ea0-105">Enhancements that have been made to the management experience for Retail product categories let merchandising managers have a correlation between Retail product hierarchy and released product details.</span></span> <span data-ttu-id="a6ea0-106">これらの拡張機能を表示するには、**カテゴリと製品の管理**ワークスペースで、[Retail 製品階層] を選択して [Retail 製品カテゴリの新しい構造] ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="a6ea0-106">To view these enhancements, in the **Category & product management**  workspace, select **Retail product hierarchy** to open the **New structure of Retail product category** page.</span></span> 

<span data-ttu-id="a6ea0-107">以前のリリースでは、適用性の範囲に基づいて、製品のプロパティが Basic 製品のプロパティと Retail 製品のプロパティに分割されていました。</span><span class="sxs-lookup"><span data-stu-id="a6ea0-107">In previous releases, product properties were divided into Basic product properties and Retail product properties, based on the scope of their applicability.</span></span> <span data-ttu-id="a6ea0-108">Retail 製品のプロパティは*グローバル*でした。</span><span class="sxs-lookup"><span data-stu-id="a6ea0-108">Retail product properties were *global*.</span></span> <span data-ttu-id="a6ea0-109">つまり、特定の製品のプロパティに、すべての法人で同じ値が共有されます。</span><span class="sxs-lookup"><span data-stu-id="a6ea0-109">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="a6ea0-110">Basic 製品のプロパティは*法人固有*でした。</span><span class="sxs-lookup"><span data-stu-id="a6ea0-110">Basic product properties were *legal entity–specific*.</span></span> <span data-ttu-id="a6ea0-111">つまり、特定の製品のプロパティは、個々の業務要件に基づいて、法人間で異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="a6ea0-111">In other words, a given product property might differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="a6ea0-112">これらの拡張機能では、Retail 製品カテゴリの製品のプロパティについて、グループ内の適用性に基づいて引き続きフィールドを区切り、リリース済製品の詳細フォームの構造を反映します。</span><span class="sxs-lookup"><span data-stu-id="a6ea0-112">With these enhancements, for product properties in the Retail product category, we continue to separate the fields, based on their applicability within a group, to reflect the released product details form structure.</span></span>

<span data-ttu-id="a6ea0-113">法人特定のプロパティをすべての法人で管理するか、特定の法人用に管理するかのどちらかに切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="a6ea0-113">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="a6ea0-114">必要に応じて、[すべての法人用に表示/編集] または [特定の法人用に表示/編集] のいずれかを選択するだけです。</span><span class="sxs-lookup"><span data-stu-id="a6ea0-114">Just select **View/Edit for all legal entities** or **View/Edit for a specific legal entity** as you require.</span></span>

<span data-ttu-id="a6ea0-115">販売促進マネージャーは、個々のカテゴリのレベルで製品のプロパティの追加のセットに既定値を定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="a6ea0-115">Merchandising managers can also define default values for an additional set of product properties at the level of an individual category.</span></span> <span data-ttu-id="a6ea0-116">これらのプロパティ値は、製品の作成時に、カテゴリとの関連に基づいて製品に継承されます。</span><span class="sxs-lookup"><span data-stu-id="a6ea0-116">These property values are inherited by a product, based on their association with a category at the time of product creation.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="a6ea0-117">プロパティを選択して Retail 製品カテゴリ フォームから製品を更新する</span><span class="sxs-lookup"><span data-stu-id="a6ea0-117">Select properties to update products from the Retail product category form</span></span>

<span data-ttu-id="a6ea0-118">論理グループのプロパティを使用して、関連付けられた製品にプッシュされる更新済の製品のプロパティを選択します。</span><span class="sxs-lookup"><span data-stu-id="a6ea0-118">You can use logical grouping properties to select which updated product properties should be pushed to associated products.</span></span>

<span data-ttu-id="a6ea0-119">販売促進マネージャーは、個々の業務要件を満たすために、各製品のこれらの継承された製品プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="a6ea0-119">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>

