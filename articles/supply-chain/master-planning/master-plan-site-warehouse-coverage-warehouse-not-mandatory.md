---
title: マスター プラン - サイトと倉庫の補充、倉庫は必須ではない
description: このトピックでは、サイトおよび倉庫の補充分析コードを持つ品目の計画方法について説明します。 倉庫分析コードが必須ではありません。
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5df79b8ea9ab6e37960cfbf0ca0edcbbc21484db
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213633"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a><span data-ttu-id="f4387-104">マスター プラン - サイトと倉庫の補充、倉庫は必須ではない</span><span class="sxs-lookup"><span data-stu-id="f4387-104">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4387-105">このトピックでは、サイトおよび倉庫の補充分析コードを持つ品目の計画方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f4387-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="f4387-106">倉庫分析コードが必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="f4387-106">The warehouse dimension is not mandatory.</span></span>

<span data-ttu-id="f4387-107">このマスター計画シナリオの前提条件を次に示します。</span><span class="sxs-lookup"><span data-stu-id="f4387-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="f4387-108">サイト分析コードが必須に設定され、需要トランザクションで入力されている。</span><span class="sxs-lookup"><span data-stu-id="f4387-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="f4387-109">この設定は変更できません。</span><span class="sxs-lookup"><span data-stu-id="f4387-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="f4387-110">倉庫分析コードが必須に設定されていない。</span><span class="sxs-lookup"><span data-stu-id="f4387-110">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="f4387-111">倉庫は既知である場合もあるが、マスタ 計画計算には使用されない。</span><span class="sxs-lookup"><span data-stu-id="f4387-111">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="f4387-112">サイト分析コードおよび倉庫分析コードが補充計画に対して設定されている。</span><span class="sxs-lookup"><span data-stu-id="f4387-112">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="f4387-113">他の分析コードが補充計画に対して設定されている場合もある。</span><span class="sxs-lookup"><span data-stu-id="f4387-113">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="f4387-114">ただし、これらはマルチサイト機能の影響を受けない。</span><span class="sxs-lookup"><span data-stu-id="f4387-114">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="f4387-115">次の図は、マスター計画がどのように進行するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="f4387-115">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="f4387-116">図の中で使用されているパラメータとその設定場所を次に示します。</span><span class="sxs-lookup"><span data-stu-id="f4387-116">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="f4387-117">倉庫は [手動] に設定されています。</span><span class="sxs-lookup"><span data-stu-id="f4387-117">The warehouse is set to Manual.</span></span> <span data-ttu-id="f4387-118">**在庫管理] &gt; [設定] &gt; [在庫詳細] &gt; [倉庫** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4387-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="f4387-119">**マスター計画** クイック タブに、**手動** フィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4387-119">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="f4387-120">品目に対して品目補充が定義されています。</span><span class="sxs-lookup"><span data-stu-id="f4387-120">Item coverage is defined for the item.</span></span> <span data-ttu-id="f4387-121">**製品情報管理] &gt; [製品] &gt; [リリースされた製品** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4387-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="f4387-122">品目を選択し、[アクション ウィンドウ] の **計画** タブで、**品目補充** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4387-122">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="f4387-123">倉庫に対して補充関係が定義されています。</span><span class="sxs-lookup"><span data-stu-id="f4387-123">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="f4387-124">**在庫管理] &gt; [設定] &gt; [在庫詳細] &gt; [倉庫** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4387-124">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="f4387-125">**マスター計画** クイック タブに、**主要倉庫** フィールド グループが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4387-125">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="f4387-126">既定の注文タイプには [生産]、[発注書] または [かんばん] が設定されます。</span><span class="sxs-lookup"><span data-stu-id="f4387-126">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="f4387-127">**製品情報管理] &gt; [製品] &gt; [リリースされた製品** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4387-127">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="f4387-128">品目を選択し、[アクション ウィンドウ] の **計画** タブで、**既定の注文設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4387-128">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="f4387-129">**既定の注文設定** フォームの **既定の注文タイプ** を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f4387-129">In the **Default order settings** form, see the **Default order type**.</span></span>

![サイトと倉庫の補充が必要、倉庫は必須ではない    ](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="f4387-131">追加リソース</span><span class="sxs-lookup"><span data-stu-id="f4387-131">Additional resources</span></span>
--------

[<span data-ttu-id="f4387-132">マスター プランとマルチサイト機能の概要</span><span class="sxs-lookup"><span data-stu-id="f4387-132">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="f4387-133">マスター プラン - サイトの補充、倉庫は必須</span><span class="sxs-lookup"><span data-stu-id="f4387-133">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="f4387-134">マスター プラン - サイトと倉庫の補充、倉庫は必須</span><span class="sxs-lookup"><span data-stu-id="f4387-134">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="f4387-135">マスター プラン - サイトと倉庫の補充、倉庫は必須ではない</span><span class="sxs-lookup"><span data-stu-id="f4387-135">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="f4387-136">BOM バージョンの決定</span><span class="sxs-lookup"><span data-stu-id="f4387-136">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



