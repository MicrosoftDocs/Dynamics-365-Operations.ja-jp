---
title: "マスタ プランとマルチサイト機能"
description: "マスター プランでは、サイトと倉庫の在庫分析コードの設定が考慮されます。"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 04f61141497570577520fe9146fbd1464f31062e
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---

# <a name="master-planning-and-multisite-functionality"></a><span data-ttu-id="3c28b-103">マスタ プランとマルチサイト機能</span><span class="sxs-lookup"><span data-stu-id="3c28b-103">Master planning and multisite functionality</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3c28b-104">マスター プランでは、サイトと倉庫の在庫分析コードの設定が考慮されます。</span><span class="sxs-lookup"><span data-stu-id="3c28b-104">Master planning takes the settings of the site and warehouse inventory dimensions into account.</span></span> 

<span data-ttu-id="3c28b-105">サイト分析コードは必須になり、倉庫分析コードを必須に設定できます。</span><span class="sxs-lookup"><span data-stu-id="3c28b-105">The site dimension is mandatory, and you can set the warehouse dimension to be mandatory.</span></span>

<span data-ttu-id="3c28b-106">分析コードが必須の場合は、分析コード値をすべての在庫トランザクションに入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c28b-106">When a dimension is mandatory, a dimension value must be entered on all inventory transactions.</span></span> <span data-ttu-id="3c28b-107">このため、マスター プラン時には、初期需要があるサイトと倉庫は明らかになっています。</span><span class="sxs-lookup"><span data-stu-id="3c28b-107">Therefore, during master planning, the site and the warehouse for the initial demand are known.</span></span> <span data-ttu-id="3c28b-108">また、サイト分析コードは、下位レベルの補充展開時にサイト値が変わらないように一貫しています。</span><span class="sxs-lookup"><span data-stu-id="3c28b-108">The site dimension is also consistent so that during the explosion of lower-level demand, the site value does not change.</span></span>

<span data-ttu-id="3c28b-109">倉庫が必須に設定されていない場合は、初期需要が不明である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3c28b-109">When the warehouse is not set to mandatory, it may not be known from the initial demand.</span></span> <span data-ttu-id="3c28b-110">計画エンジンは、品目、各倉庫、および注文明細の詳細に対して定義されている設定に基づいて、使用する倉庫を決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c28b-110">The planning engine must determine which warehouse to use based on the settings that are defined for the item, individual warehouses, and the details of the order line.</span></span>

<span data-ttu-id="3c28b-111">次のトピックでは、使用する倉庫を決定するために計画エンジンを使用する方法について、定義されている各種の設定ごとに説明します。</span><span class="sxs-lookup"><span data-stu-id="3c28b-111">The following topics describe how the planning engine works, when different settings are defined, to determine the warehouse to use.</span></span>

[<span data-ttu-id="3c28b-112">マスター プラン - サイトと倉庫の補充、倉庫は必須</span><span class="sxs-lookup"><span data-stu-id="3c28b-112">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="3c28b-113">マスター プラン - サイトの補充、倉庫は必須</span><span class="sxs-lookup"><span data-stu-id="3c28b-113">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="3c28b-114">マスター プラン - サイトと倉庫の補充、倉庫は必須ではない</span><span class="sxs-lookup"><span data-stu-id="3c28b-114">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="3c28b-115">マスター プラン - サイトの補充、倉庫は必須ではない</span><span class="sxs-lookup"><span data-stu-id="3c28b-115">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="3c28b-116">マスター プラン - BOM バージョンを決定する方法</span><span class="sxs-lookup"><span data-stu-id="3c28b-116">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




