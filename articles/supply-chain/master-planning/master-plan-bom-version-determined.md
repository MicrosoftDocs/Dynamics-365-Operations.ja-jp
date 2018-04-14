---
title: "BOM バージョンの決定"
description: "需要の展開中に、品目の既定のオーダー タイプが生産になっている場合、計画エンジンはサイトに基づいて有効な BOM バージョンを探します。"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d7d66f8b498f7a55446b80245561b292cadfa9b4
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="determine-the-bom-version"></a><span data-ttu-id="41292-103">BOM バージョンの決定</span><span class="sxs-lookup"><span data-stu-id="41292-103">Determine the BOM version</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="41292-104">需要の展開中に、品目の既定のオーダー タイプが生産になっている場合、計画エンジンはサイトに基づいて有効な BOM バージョンを探します。</span><span class="sxs-lookup"><span data-stu-id="41292-104">During a demand explosion, if an item has a default order type of Production, the planning engine finds a valid BOM version based on the site.</span></span> 

<span data-ttu-id="41292-105">サイト分析コードは常に既知で、需要トランザクションに記述されています。</span><span class="sxs-lookup"><span data-stu-id="41292-105">The site dimension is always known and is stated on the demand transaction.</span></span> <span data-ttu-id="41292-106">使用する BOM バージョンを決定するには、次のプロセスを使用します。</span><span class="sxs-lookup"><span data-stu-id="41292-106">The following process is used to determine the BOM version to use:</span></span>

-   <span data-ttu-id="41292-107">品目の BOM バージョンが需要サイトで定義されている場合は、このサイト固有の BOM が使用されます。</span><span class="sxs-lookup"><span data-stu-id="41292-107">If there is a BOM version defined for the item at the demand site, the site-specific BOM is used.</span></span>
-   <span data-ttu-id="41292-108">品目のサイト固有の BOM バージョンが需要サイトで定義されていない場合は、汎用 BOM が使用されます。</span><span class="sxs-lookup"><span data-stu-id="41292-108">If there is no site-specific BOM version defined for an item at the demand site, a general BOM is used.</span></span> <span data-ttu-id="41292-109">汎用 BOM はサイト固有ではなく、複数のサイトに対して有効です。</span><span class="sxs-lookup"><span data-stu-id="41292-109">A general BOM does not state a site, and it is valid for multiple sites.</span></span> <span data-ttu-id="41292-110">汎用 BOM がある場合は、その BOM が使用されます。</span><span class="sxs-lookup"><span data-stu-id="41292-110">If there is a general BOM, it is used.</span></span>
-   <span data-ttu-id="41292-111">使用できる汎用 BOM のバージョンがない場合、需要の展開はここで停止します。</span><span class="sxs-lookup"><span data-stu-id="41292-111">If there is no general BOM version to use, the demand explosion stops at this point.</span></span>

<span data-ttu-id="41292-112">サイト固有の BOM であるか、または汎用 BOM であるかにかかわらず、有効な BOM バージョンは、必要な日付と数量の基準を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="41292-112">A valid BOM version, whether site-specific or general, must meet the required criteria for date and quantity.</span></span>






