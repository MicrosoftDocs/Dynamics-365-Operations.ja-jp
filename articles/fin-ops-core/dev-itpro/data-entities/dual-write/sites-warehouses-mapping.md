---
title: 統合されたサイトおよび倉庫
description: このトピックでは、Finance and Operations と Dataverse 間のサイトおよび倉庫データの統合について説明します。
author: t-benebo
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 533635ece005636dcee4e24d1d132111e1e2b370
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750669"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="ddbb8-103">統合されたサイトおよび倉庫</span><span class="sxs-lookup"><span data-stu-id="ddbb8-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="ddbb8-104">このトピックでは、Finance and Operations と Dataverse 間のサイトおよび倉庫データの統合について説明します。</span><span class="sxs-lookup"><span data-stu-id="ddbb8-104">This topic describes the integration of site and warehouse data between Finance and Operations and Dataverse.</span></span> <span data-ttu-id="ddbb8-105">運営サイトおよび倉庫は、Supply Chain Management における共通の概念です。</span><span class="sxs-lookup"><span data-stu-id="ddbb8-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="ddbb8-106">これらは会社のサプライ チェーンをモデル化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ddbb8-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="ddbb8-107">テンプレート</span><span class="sxs-lookup"><span data-stu-id="ddbb8-107">Templates</span></span>

<span data-ttu-id="ddbb8-108">Dataverse との統合により、これらの概念とすべての関連情報は、次の表のサイトおよび倉庫データ テーブルを使用する Dataverse で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="ddbb8-108">With the integration with Dataverse, these concepts and all their related information are available in Dataverse using the sites and warehouses data tables in the following table.</span></span>

<span data-ttu-id="ddbb8-109">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="ddbb8-109">Finance and Operations apps</span></span> | <span data-ttu-id="ddbb8-110">その他の Dynamics 365 アプリ</span><span class="sxs-lookup"><span data-stu-id="ddbb8-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="ddbb8-111">説明</span><span class="sxs-lookup"><span data-stu-id="ddbb8-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="ddbb8-112">サイト</span><span class="sxs-lookup"><span data-stu-id="ddbb8-112">Sites</span></span> | <span data-ttu-id="ddbb8-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="ddbb8-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="ddbb8-114">倉庫</span><span class="sxs-lookup"><span data-stu-id="ddbb8-114">Warehouses</span></span> | <span data-ttu-id="ddbb8-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="ddbb8-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]