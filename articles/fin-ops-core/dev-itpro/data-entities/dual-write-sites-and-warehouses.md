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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 4cf402e2811aaf92ddfa78eaf6d8887d88d93cbc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770994"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="fd73f-103">統合されたサイトおよび倉庫</span><span class="sxs-lookup"><span data-stu-id="fd73f-103">Integrated sites and warehouses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd73f-104">このトピックでは、Finance and Operations と Common Data Service 間のサイトおよび倉庫データの統合について説明します。</span><span class="sxs-lookup"><span data-stu-id="fd73f-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="fd73f-105">運営サイトおよび倉庫は、Supply Chain Management における共通の概念です。</span><span class="sxs-lookup"><span data-stu-id="fd73f-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="fd73f-106">これらは会社のサプライ チェーンをモデル化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fd73f-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="fd73f-107">テンプレート</span><span class="sxs-lookup"><span data-stu-id="fd73f-107">Templates</span></span>

<span data-ttu-id="fd73f-108">Common Data Service との統合により、これらの概念とすべての関連情報は、次の表のサイトおよび倉庫データ エンティティを使用する Common Data Service で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="fd73f-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="fd73f-109">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="fd73f-109">Finance and Operations apps</span></span> | <span data-ttu-id="fd73f-110">その他の Dynamics 365 アプリ</span><span class="sxs-lookup"><span data-stu-id="fd73f-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="fd73f-111">説明</span><span class="sxs-lookup"><span data-stu-id="fd73f-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="fd73f-112">サイト</span><span class="sxs-lookup"><span data-stu-id="fd73f-112">Sites</span></span> | <span data-ttu-id="fd73f-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="fd73f-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="fd73f-114">倉庫</span><span class="sxs-lookup"><span data-stu-id="fd73f-114">Warehouses</span></span> | <span data-ttu-id="fd73f-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="fd73f-115">msdyn_warehouses</span></span> | 

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [operational sites](dual-write/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](dual-write/InventWarehouseEntity-msdyn-warehouse.md)]

