---
title: "小売製品カテゴリと製品を管理します。"
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
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 0bcc5989edd9913fce414c0c24068f111d8c1aeb
ms.contentlocale: ja-jp
ms.lasthandoff: 01/04/2019

---

# <a name="manage-retail-product-categories-and-products"></a><span data-ttu-id="16dae-103">小売製品カテゴリと製品を管理します。</span><span class="sxs-lookup"><span data-stu-id="16dae-103">Manage Retail product categories and products</span></span>

[!include [banner](./includes/banner.md)]

<span data-ttu-id="16dae-104">このトピックでは、Microsoft Dynamics 365 for Retail の小売製品カテゴリと製品を管理するための強化された方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="16dae-104">This topic describes an enhanced way to manage Retail product categories and products in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="16dae-105">拡張機能で、販売促進マネージャーは小売製品階層、およびリリース済製品の詳細の間で共有されている製品プロパティの構造を表示できます。</span><span class="sxs-lookup"><span data-stu-id="16dae-105">The enhancements let merchandising managers view a structure of product properties that is shared between the Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="16dae-106">小売製品カテゴリの管理に関する詳細については、**カテゴリと製品の管理**ワークスペースの、**小売製品階層**タイルを選択してください。</span><span class="sxs-lookup"><span data-stu-id="16dae-106">To learn more about how to manage Retail product categories, in the **Category and product management** workspace, select the **Retail product hierarchy** tile.</span></span>

<span data-ttu-id="16dae-107">表示される **小売製品階層** ページの強化された構造を確認します。</span><span class="sxs-lookup"><span data-stu-id="16dae-107">Notice the enhanced structure of the **Retail product hierarchy** page that appears.</span></span> <span data-ttu-id="16dae-108">Retail の以前のバージョンでは、製品のプロパティは適用性の範囲に基づいて [*基本的な製品プロパティ*] と [*小売製品プロパティ*] に分割されていました。</span><span class="sxs-lookup"><span data-stu-id="16dae-108">In previous versions of Retail, product properties were divided into *basic product properties* and *Retail product properties*, based on the scope of their applicability.</span></span> <span data-ttu-id="16dae-109">小売製品プロパティは適用範囲が*グローバル*です。</span><span class="sxs-lookup"><span data-stu-id="16dae-109">Retail product properties are *global* in their scope of applicability.</span></span> <span data-ttu-id="16dae-110">つまり、特定の小売製品のプロパティに、すべての法人で同じ値が共有されます。</span><span class="sxs-lookup"><span data-stu-id="16dae-110">In other words, for a given Retail product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="16dae-111">対照的に、基本的な製品プロパティは*法人固有*です。</span><span class="sxs-lookup"><span data-stu-id="16dae-111">By contrast, basic product properties are *legal entity–specific*.</span></span> <span data-ttu-id="16dae-112">つまり、特定の製品のプロパティでは、各法人の個々の業務要件に応じて、法人間で値が異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="16dae-112">In other words, for a given basic product property, the value can differ across legal entities, depending on the individual business requirements of each legal entity.</span></span>

<span data-ttu-id="16dae-113">拡張された小売製品カテゴリ構造では、リリースされた製品の詳細フォーム構造の構造を反映するために、グループの適用性に基づいて製品プロパティが論理的に分離されます。</span><span class="sxs-lookup"><span data-stu-id="16dae-113">In the enhanced Retail product category structure, product properties are logically separated based on their applicability in a group, to reflect the structure of the released product details form structure.</span></span>

![フィールドはプロパティの適用範囲に基づいてグループ化されます。](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="16dae-115">法人特定のプロパティをすべての法人で管理するか、特定の法人用に管理するかのどちらかに切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="16dae-115">You can switch between managing legal entity–specific properties across all legal entities and managing them for a specific legal entity.</span></span>

<span data-ttu-id="16dae-116">すべての法人の間でプロパティを管理するには、**すべての法人用に表示** (または**すべての法人用に編集**) を選択してください。</span><span class="sxs-lookup"><span data-stu-id="16dae-116">To manage properties across all legal entities, select **View for all legal entities** (or **Edit for all legal entities**).</span></span>

![すべての法人用に表示/編集](media/ToggleBackToEditForSpecificLegalEntity.PNG)

<span data-ttu-id="16dae-118">特定の法人のプロパティを管理するには、**特定の法人用に表示** (または**特定の法人用に編集**) を選択してください。</span><span class="sxs-lookup"><span data-stu-id="16dae-118">To manage properties for a specific legal entity, select **View for a specific legal entity** (or **Edit for a specific legal entity**).</span></span>

![特定の法人用に表示/編集](media/ToggleToEditForAllLegalEntities.PNG)

<span data-ttu-id="16dae-120">また、拡張された小売製品カテゴリ構造では、販売促進マネージャーが、個々のカテゴリ レベルで追加の製品プロパティ セットの既定値を定義できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="16dae-120">Additionally, in the enhanced Retail product category structure, a merchandising manager can now define default values for an additional set of product properties at the level of the individual category.</span></span> <span data-ttu-id="16dae-121">次に、製品が作成されると、小売製品階層内の個々のカテゴリとそれらのプロパティの関連付けに基づいて、製品プロパティの既定値が継承されます。</span><span class="sxs-lookup"><span data-stu-id="16dae-121">Then, when products are created, they inherit default values for their product properties, based on the association of those properties with an individual category in Retail product hierarchy.</span></span> <span data-ttu-id="16dae-122">これらの継承された製品プロパティは、個々の業務要件を満たすために製品ごとに変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="16dae-122">These inherited product properties can also be modified for each product to meet individual business requirements.</span></span>

## <a name="selecting-properties-to-update-products-on-the-retail-product-hierarchy-page"></a><span data-ttu-id="16dae-123">Retail 製品階層ページで製品を更新するためのプロパティの選択</span><span class="sxs-lookup"><span data-stu-id="16dae-123">Selecting properties to update products on the Retail product hierarchy page</span></span>

<span data-ttu-id="16dae-124">新しい、拡張された製品プロパティ構造を使用して、関連付けられた製品にプッシュされる必要がある更新された製品プロパティを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="16dae-124">You can use the new enhanced structure for product properties to select updated product properties that must be pushed to the associated products.</span></span> <span data-ttu-id="16dae-125">**小売製品階層** ページのアクション ウィンドウで、**カテゴリ**を選択し、次に**製品の更新**を選択して **製品の更新** ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="16dae-125">On the **Retail product hierarchy** page, on the Action Pane, select **Category**, and then select **Update products** to open the **Update products** dialog box.</span></span>

![製品の更新ダイアログ ボックス](media/NewUpdateProductsEnhancedView.PNG)

