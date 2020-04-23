---
title: マスター プラン - サイトと倉庫の補充、倉庫は必須
description: このトピックでは、サイトおよび倉庫の補充分析コードを持つ品目の計画方法について説明します。 倉庫分析コードは必須です。
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
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df35389176368c44c2ff4a3210fabc25bf24c807
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213679"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a><span data-ttu-id="162fb-104">マスター プラン - サイトと倉庫の補充、倉庫は必須</span><span class="sxs-lookup"><span data-stu-id="162fb-104">Master planning for site and warehouse coverage, warehouse mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="162fb-105">このトピックでは、サイトおよび倉庫の補充分析コードを持つ品目の計画方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="162fb-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="162fb-106">倉庫分析コードは必須です。</span><span class="sxs-lookup"><span data-stu-id="162fb-106">The warehouse dimension is mandatory.</span></span>

<span data-ttu-id="162fb-107">このマスター計画シナリオの前提条件を次に示します。</span><span class="sxs-lookup"><span data-stu-id="162fb-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="162fb-108">サイト分析コードが必須に設定され、需要トランザクションで入力されている。</span><span class="sxs-lookup"><span data-stu-id="162fb-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="162fb-109">倉庫分析コードが必須に設定され、需要トランザクションで入力されている。</span><span class="sxs-lookup"><span data-stu-id="162fb-109">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="162fb-110">サイト分析コードおよび倉庫分析コードが補充計画用に設定されている。</span><span class="sxs-lookup"><span data-stu-id="162fb-110">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="162fb-111">他の分析コードが補充計画に対して設定されている場合もある。</span><span class="sxs-lookup"><span data-stu-id="162fb-111">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="162fb-112">ただし、これらはマルチサイト機能の影響を受けない。</span><span class="sxs-lookup"><span data-stu-id="162fb-112">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="162fb-113">次の図は、マスター計画がどのように進行するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="162fb-113">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="162fb-114">図の中で使用されているパラメータとその設定場所を次に示します。</span><span class="sxs-lookup"><span data-stu-id="162fb-114">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="162fb-115">倉庫は **手動** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="162fb-115">The warehouse is set to **Manual**.</span></span> <span data-ttu-id="162fb-116">**在庫管理] &gt; [設定] &gt; [在庫詳細] &gt; [倉庫** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="162fb-116">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="162fb-117">**マスター計画** クイック タブに、**手動** フィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="162fb-117">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="162fb-118">品目に対して品目補充が定義されています。</span><span class="sxs-lookup"><span data-stu-id="162fb-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="162fb-119">**製品情報管理] &gt; [製品] &gt; [リリースされた製品** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="162fb-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="162fb-120">品目を選択し、[アクション ウィンドウ] の **計画** タブで、**品目補充** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="162fb-120">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="162fb-121">倉庫に対して補充関係が定義されています。</span><span class="sxs-lookup"><span data-stu-id="162fb-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="162fb-122">**在庫管理] &gt; [設定] &gt; [在庫詳細] &gt; [倉庫** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="162fb-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="162fb-123">**マスター計画** クイック タブに、**主要倉庫** フィールド グループが表示されます。</span><span class="sxs-lookup"><span data-stu-id="162fb-123">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="162fb-124">既定の注文タイプには [生産]、[発注書] または [かんばん] が設定されます。</span><span class="sxs-lookup"><span data-stu-id="162fb-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="162fb-125">**製品情報管理] &gt; [製品] &gt; [リリースされた製品** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="162fb-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="162fb-126">品目を選択し、[アクション ウィンドウ] の **計画** タブで、**既定の注文設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="162fb-126">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="162fb-127">**既定の注文設定** フォームの **既定の注文タイプ** を参照してください。</span><span class="sxs-lookup"><span data-stu-id="162fb-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![サイトと倉庫の補充が必要、倉庫は必須    ](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="162fb-129">追加リソース</span><span class="sxs-lookup"><span data-stu-id="162fb-129">Additional resources</span></span>
--------

[<span data-ttu-id="162fb-130">マスター プランとマルチサイト機能の概要</span><span class="sxs-lookup"><span data-stu-id="162fb-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="162fb-131">マスター プラン - サイトの補充、倉庫は必須</span><span class="sxs-lookup"><span data-stu-id="162fb-131">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="162fb-132">マスター プラン - サイトの補充、倉庫は必須ではない</span><span class="sxs-lookup"><span data-stu-id="162fb-132">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="162fb-133">マスター プラン - サイトと倉庫の補充、倉庫は必須ではない</span><span class="sxs-lookup"><span data-stu-id="162fb-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="162fb-134">BOM バージョンの決定</span><span class="sxs-lookup"><span data-stu-id="162fb-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



