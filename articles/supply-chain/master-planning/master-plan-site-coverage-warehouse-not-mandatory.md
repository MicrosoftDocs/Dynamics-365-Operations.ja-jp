---
title: マスター プラン - サイトの補充、倉庫は必須ではない
description: このトピックでは、サイト分析コードを品目補充用に持つ品目の計画方法について説明します。
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
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fe5cb5f9d21afcd12f3041bb9acc89fff360c95e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970459"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a><span data-ttu-id="6f7dc-103">マスター プラン - サイトの補充、倉庫は必須ではない</span><span class="sxs-lookup"><span data-stu-id="6f7dc-103">Master planning for site coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f7dc-104">このトピックでは、サイト分析コードを品目補充用に持つ品目の計画方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6f7dc-104">This topic describes how an item that has the site dimension set for coverage is planned.</span></span>

<span data-ttu-id="6f7dc-105">このマスター計画シナリオの前提条件を次に示します。</span><span class="sxs-lookup"><span data-stu-id="6f7dc-105">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="6f7dc-106">サイト分析コードが必須に設定され、需要トランザクションで入力されている。</span><span class="sxs-lookup"><span data-stu-id="6f7dc-106">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="6f7dc-107">倉庫分析コードが必須に設定されていない。</span><span class="sxs-lookup"><span data-stu-id="6f7dc-107">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="6f7dc-108">倉庫は既知である場合もあるが、マスタ 計画計算には使用されない。</span><span class="sxs-lookup"><span data-stu-id="6f7dc-108">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="6f7dc-109">サイト分析コードが補充計画用に設定されている。</span><span class="sxs-lookup"><span data-stu-id="6f7dc-109">The site dimension is set for coverage planning.</span></span>
-   <span data-ttu-id="6f7dc-110">倉庫分析コードが補充計画用に設定されていない。</span><span class="sxs-lookup"><span data-stu-id="6f7dc-110">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="6f7dc-111">そのため、供給と需要はサイトごとに集計され、多分、他の補充計画分析コードも同様です。</span><span class="sxs-lookup"><span data-stu-id="6f7dc-111">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="6f7dc-112">次の図は、マスター計画がどのように進行するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="6f7dc-112">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="6f7dc-113">図の中で使用されているパラメータとその設定場所を次に示します。</span><span class="sxs-lookup"><span data-stu-id="6f7dc-113">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="6f7dc-114">品目に対して品目補充が定義されています。</span><span class="sxs-lookup"><span data-stu-id="6f7dc-114">Item coverage is defined for the item.</span></span> <span data-ttu-id="6f7dc-115">**製品情報管理] &gt; [製品] &gt; [リリースされた製品** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f7dc-115">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="6f7dc-116">品目を選択し、**計画] &gt; [品目補充** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f7dc-116">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="6f7dc-117">倉庫に対して補充関係が定義されています。</span><span class="sxs-lookup"><span data-stu-id="6f7dc-117">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="6f7dc-118">**在庫管理] &gt; [設定] &gt; [在庫詳細] &gt; [倉庫** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f7dc-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="6f7dc-119">**マスター計画** タブに、**主要倉庫** フィールド グループが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6f7dc-119">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="6f7dc-120">既定の注文タイプは [生産]、[発注書] または [かんばん] に設定されます。</span><span class="sxs-lookup"><span data-stu-id="6f7dc-120">The default order type is set to Production, Purchase order or Kanban.</span></span> <span data-ttu-id="6f7dc-121">**製品情報管理] &gt; [製品] &gt; [リリースされた製品** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f7dc-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="6f7dc-122">品目を選択し、**計画] &gt; [既定の注文設定** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f7dc-122">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="6f7dc-123">**既定の注文設定** フォームの **既定の注文タイプ** フィールドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f7dc-123">In the **Default order settings** form, see the **Default order type** field.</span></span>

![サイトの補充が必要、倉庫は必須ではない    ](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="6f7dc-125">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6f7dc-125">Additional resources</span></span>
--------

[<span data-ttu-id="6f7dc-126">マスター プランとマルチサイト機能の概要</span><span class="sxs-lookup"><span data-stu-id="6f7dc-126">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="6f7dc-127">マスター プラン - サイトと倉庫の補充、倉庫は必須</span><span class="sxs-lookup"><span data-stu-id="6f7dc-127">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="6f7dc-128">マスター プラン - サイトの補充、倉庫は必須</span><span class="sxs-lookup"><span data-stu-id="6f7dc-128">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="6f7dc-129">マスター プラン - サイトの補充、倉庫は必須ではない</span><span class="sxs-lookup"><span data-stu-id="6f7dc-129">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="6f7dc-130">BOM バージョンの決定</span><span class="sxs-lookup"><span data-stu-id="6f7dc-130">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



