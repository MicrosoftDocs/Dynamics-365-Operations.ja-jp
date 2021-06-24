---
title: マスター プラン - サイトの補充、倉庫は必須
description: このトピックでは、補充分析コードとしてサイトを持つ品目の計画方法について説明します。 倉庫は必須の分析コードです。
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 008061d286505a2e678e15fbff7706da9c410dfe
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187557"
---
# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a><span data-ttu-id="5eb1a-104">マスター プラン - サイトの補充、倉庫は必須</span><span class="sxs-lookup"><span data-stu-id="5eb1a-104">Master planning for site coverage, mandatory warehouse</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5eb1a-105">このトピックでは、補充分析コードとしてサイトを持つ品目の計画方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5eb1a-105">This topic describes how an item that has the site as coverage dimension is planned.</span></span> <span data-ttu-id="5eb1a-106">倉庫は必須の分析コードです。</span><span class="sxs-lookup"><span data-stu-id="5eb1a-106">Warehouse is a mandatory dimension.</span></span>

<span data-ttu-id="5eb1a-107">このマスター計画シナリオの前提条件を次に示します。</span><span class="sxs-lookup"><span data-stu-id="5eb1a-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="5eb1a-108">サイト分析コードが必須に設定され、需要トランザクションで入力されている。</span><span class="sxs-lookup"><span data-stu-id="5eb1a-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="5eb1a-109">この設定は変更できません。</span><span class="sxs-lookup"><span data-stu-id="5eb1a-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="5eb1a-110">倉庫分析コードが必須に設定され、需要トランザクションで入力されている。</span><span class="sxs-lookup"><span data-stu-id="5eb1a-110">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="5eb1a-111">サイト分析コードが補充計画用に設定されている。</span><span class="sxs-lookup"><span data-stu-id="5eb1a-111">The site dimension is set for coverage planning.</span></span> <span data-ttu-id="5eb1a-112">他の分析コードが補充計画に対して設定されている場合もある。</span><span class="sxs-lookup"><span data-stu-id="5eb1a-112">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="5eb1a-113">ただし、これらはマルチサイト機能の影響を受けない。</span><span class="sxs-lookup"><span data-stu-id="5eb1a-113">However, they are not affected by the multisite functionality.</span></span>
-   <span data-ttu-id="5eb1a-114">倉庫分析コードが補充計画用に設定されていない。</span><span class="sxs-lookup"><span data-stu-id="5eb1a-114">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="5eb1a-115">そのため、供給と需要はサイトごとに集計され、多分、他の補充計画分析コードも同様です。</span><span class="sxs-lookup"><span data-stu-id="5eb1a-115">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="5eb1a-116">次の図は、マスター計画がどのように進行するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="5eb1a-116">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="5eb1a-117">図の中で使用されているパラメータとその設定場所を次に示します。</span><span class="sxs-lookup"><span data-stu-id="5eb1a-117">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="5eb1a-118">品目に対して品目補充が定義されています。</span><span class="sxs-lookup"><span data-stu-id="5eb1a-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="5eb1a-119">**製品情報管理] &gt; [製品] &gt; [リリースされた製品** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="5eb1a-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="5eb1a-120">品目を選択し、**計画] &gt; [品目補充** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="5eb1a-120">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="5eb1a-121">倉庫に対して補充関係が定義されています。</span><span class="sxs-lookup"><span data-stu-id="5eb1a-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="5eb1a-122">**在庫管理] &gt; [設定] &gt; [在庫詳細] &gt; [倉庫** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="5eb1a-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="5eb1a-123">**マスター計画** タブに、**主要倉庫** フィールド グループが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5eb1a-123">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="5eb1a-124">既定の注文タイプには [生産]、[発注書] または [かんばん] が設定されます。</span><span class="sxs-lookup"><span data-stu-id="5eb1a-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="5eb1a-125">**製品情報管理] &gt; [製品] &gt; [リリースされた製品** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="5eb1a-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="5eb1a-126">品目を選択し、**計画] &gt; [既定の注文設定** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="5eb1a-126">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="5eb1a-127">**既定の注文設定** フォームの **既定の注文タイプ** を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5eb1a-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![サイトの補充が必要、倉庫は必須    ](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



## <a name="additional-resources"></a><span data-ttu-id="5eb1a-129">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5eb1a-129">Additional resources</span></span>

[<span data-ttu-id="5eb1a-130">マスター プランとマルチサイト機能の概要</span><span class="sxs-lookup"><span data-stu-id="5eb1a-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="5eb1a-131">マスター プラン - サイトと倉庫の補充、倉庫は必須</span><span class="sxs-lookup"><span data-stu-id="5eb1a-131">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="5eb1a-132">マスター プラン - サイトの補充、倉庫は必須</span><span class="sxs-lookup"><span data-stu-id="5eb1a-132">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="5eb1a-133">マスター プラン - サイトと倉庫の補充、倉庫は必須ではない</span><span class="sxs-lookup"><span data-stu-id="5eb1a-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="5eb1a-134">BOM バージョンの決定</span><span class="sxs-lookup"><span data-stu-id="5eb1a-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]