---
title: 製品カテゴリおよび製品の管理
description: このトピックでは、販売促進マネージャーが製品カテゴリを使用して、Commerce 製品階層とリリースされた製品の詳細な関係を管理する方法について説明します。
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: EcoResCategorySearchList, EcoResAttribute, COODualUseCategories, EcoResProductCategory, EcoResCategoryAddProduct, EcoResAttributeValue
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 95a4bac6beeaf5fad449027d93132fc1499288a0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215489"
---
# <a name="manage-product-categories-and-products"></a><span data-ttu-id="8a1a2-103">製品カテゴリおよび製品の管理</span><span class="sxs-lookup"><span data-stu-id="8a1a2-103">Manage product categories and products</span></span>

[!include [banner](./includes/banner.md)]

<span data-ttu-id="8a1a2-104">このトピックでは、Dynamics 365 Commerce の製品カテゴリと製品を管理するための強化された方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8a1a2-104">This topic describes an enhanced way to manage product categories and products in Dynamics 365 Commerce.</span></span> <span data-ttu-id="8a1a2-105">拡張機能で、販売促進マネージャーは製品階層、およびリリース済製品の詳細の間で共有されている製品プロパティの構造を表示できます。</span><span class="sxs-lookup"><span data-stu-id="8a1a2-105">The enhancements let merchandising managers view a structure of product properties that is shared between the product hierarchy and released product details.</span></span>

<span data-ttu-id="8a1a2-106">製品カテゴリの管理に関する詳細については、**カテゴリと製品の管理** ワークスペースの **Commerce製品階層** タイルを選択してください。</span><span class="sxs-lookup"><span data-stu-id="8a1a2-106">To learn more about how to manage product categories, in the **Category and product management** workspace, select the **Commerce product hierarchy** tile.</span></span>

<span data-ttu-id="8a1a2-107">表示される **Commerce 製品階層** ページの強化された構造を確認します。</span><span class="sxs-lookup"><span data-stu-id="8a1a2-107">Notice the enhanced structure of the **Commerce product hierarchy** page that appears.</span></span> <span data-ttu-id="8a1a2-108">アプリの以前のバージョンでは、製品のプロパティは適用性の範囲に基づいて *基本的な製品プロパティ* と *小売製品プロパティ* に分割されていました。</span><span class="sxs-lookup"><span data-stu-id="8a1a2-108">In previous versions of the app, product properties were divided into *basic product properties* and *Retail product properties*, based on the scope of their applicability.</span></span> <span data-ttu-id="8a1a2-109">小売製品プロパティは適用範囲が *グローバル* です。</span><span class="sxs-lookup"><span data-stu-id="8a1a2-109">Retail product properties are *global* in their scope of applicability.</span></span> <span data-ttu-id="8a1a2-110">つまり、特定の製品のプロパティに、すべての法人で同じ値が共有されます。</span><span class="sxs-lookup"><span data-stu-id="8a1a2-110">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="8a1a2-111">対照的に、基本的な製品プロパティは *法人固有* です。</span><span class="sxs-lookup"><span data-stu-id="8a1a2-111">By contrast, basic product properties are *legal entity–specific*.</span></span> <span data-ttu-id="8a1a2-112">つまり、特定の製品のプロパティでは、各法人の個々の業務要件に応じて、法人間で値が異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="8a1a2-112">In other words, for a given basic product property, the value can differ across legal entities, depending on the individual business requirements of each legal entity.</span></span>

<span data-ttu-id="8a1a2-113">拡張された製品カテゴリ構造では、リリースされた製品の詳細フォーム構造の構造を反映するために、グループの適用性に基づいて製品プロパティが論理的に分離されます。</span><span class="sxs-lookup"><span data-stu-id="8a1a2-113">In the enhanced product category structure, product properties are logically separated based on their applicability in a group, to reflect the structure of the released product details form structure.</span></span>

![フィールドはプロパティの適用範囲に基づいてグループ化されます。](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="8a1a2-115">法人特定のプロパティをすべての法人で管理するか、特定の法人用に管理するかのどちらかに切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="8a1a2-115">You can switch between managing legal entity–specific properties across all legal entities and managing them for a specific legal entity.</span></span>

<span data-ttu-id="8a1a2-116">すべての法人の間でプロパティを管理するには、**すべての法人用に表示** (または **すべての法人用に編集**) を選択してください。</span><span class="sxs-lookup"><span data-stu-id="8a1a2-116">To manage properties across all legal entities, select **View for all legal entities** (or **Edit for all legal entities**).</span></span>

![すべての法人用に表示/編集](media/ToggleBackToEditForSpecificLegalEntity.PNG)

<span data-ttu-id="8a1a2-118">特定の法人のプロパティを管理するには、**特定の法人用に表示** (または **特定の法人用に編集**) を選択してください。</span><span class="sxs-lookup"><span data-stu-id="8a1a2-118">To manage properties for a specific legal entity, select **View for a specific legal entity** (or **Edit for a specific legal entity**).</span></span>

![特定の法人用に表示/編集](media/ToggleToEditForAllLegalEntities.PNG)

<span data-ttu-id="8a1a2-120">また、拡張された製品カテゴリ構造では、販売促進マネージャーが、個々のカテゴリ レベルで追加の製品プロパティ セットの既定値を定義できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="8a1a2-120">Additionally, in the enhanced product category structure, a merchandising manager can now define default values for an additional set of product properties at the level of the individual category.</span></span> <span data-ttu-id="8a1a2-121">次に、製品が作成されると、製品階層内の個々のカテゴリとそれらのプロパティの関連付けに基づいて、製品プロパティの既定値が継承されます。</span><span class="sxs-lookup"><span data-stu-id="8a1a2-121">Then, when products are created, they inherit default values for their product properties, based on the association of those properties with an individual category in the product hierarchy.</span></span> <span data-ttu-id="8a1a2-122">これらの継承された製品プロパティは、個々の業務要件を満たすために製品ごとに変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="8a1a2-122">These inherited product properties can also be modified for each product to meet individual business requirements.</span></span>

## <a name="selecting-properties-to-update-products-on-the-commerce-product-hierarchy-page"></a><span data-ttu-id="8a1a2-123">Commerce 製品階層ページで製品を更新するためのプロパティの選択</span><span class="sxs-lookup"><span data-stu-id="8a1a2-123">Selecting properties to update products on the Commerce product hierarchy page</span></span>

<span data-ttu-id="8a1a2-124">新しい、拡張された製品プロパティ構造を使用して、関連付けられた製品にプッシュされる必要がある更新された製品プロパティを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="8a1a2-124">You can use the new enhanced structure for product properties to select updated product properties that must be pushed to the associated products.</span></span> <span data-ttu-id="8a1a2-125">**Commerce 製品階層** ページのアクション ウィンドウで、**カテゴリ** を選択し、次に **製品の更新** を選択して **製品の更新** ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="8a1a2-125">On the **Commerce product hierarchy** page, on the Action Pane, select **Category**, and then select **Update products** to open the **Update products** dialog box.</span></span>

![製品の更新ダイアログ ボックス](media/NewUpdateProductsEnhancedView.PNG)


[!INCLUDE[footer-include](../includes/footer-banner.md)]