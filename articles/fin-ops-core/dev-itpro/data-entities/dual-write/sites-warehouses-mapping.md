---
title: 統合されたサイトおよび倉庫
description: このトピックでは、Finance and Operations と Common Data Service 間のサイトおよび倉庫データの統合について説明します。
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: d5c2030160f6025c9de63b2c29215364f5f87e6f
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997627"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="9827d-103">統合されたサイトおよび倉庫</span><span class="sxs-lookup"><span data-stu-id="9827d-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="9827d-104">このトピックでは、Finance and Operations と Common Data Service 間のサイトおよび倉庫データの統合について説明します。</span><span class="sxs-lookup"><span data-stu-id="9827d-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="9827d-105">運営サイトおよび倉庫は、Supply Chain Management における共通の概念です。</span><span class="sxs-lookup"><span data-stu-id="9827d-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="9827d-106">これらは会社のサプライ チェーンをモデル化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9827d-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="9827d-107">テンプレート</span><span class="sxs-lookup"><span data-stu-id="9827d-107">Templates</span></span>

<span data-ttu-id="9827d-108">Common Data Service との統合により、これらの概念とすべての関連情報は、次の表のサイトおよび倉庫データ エンティティを使用する Common Data Service で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="9827d-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="9827d-109">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="9827d-109">Finance and Operations apps</span></span> | <span data-ttu-id="9827d-110">その他の Dynamics 365 アプリ</span><span class="sxs-lookup"><span data-stu-id="9827d-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="9827d-111">説明</span><span class="sxs-lookup"><span data-stu-id="9827d-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="9827d-112">サイト</span><span class="sxs-lookup"><span data-stu-id="9827d-112">Sites</span></span> | <span data-ttu-id="9827d-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="9827d-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="9827d-114">倉庫</span><span class="sxs-lookup"><span data-stu-id="9827d-114">Warehouses</span></span> | <span data-ttu-id="9827d-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="9827d-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

