---
title: Microsoft Dynamics 365 for Field Service との統合
description: このトピックでは、Microsoft Dynamics 365 for Field Service との統合の概要を提供します。
author: ChristianRytt
manager: AnnBe
ms.date: 02/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: efda4e39f63155785386ecec6d21973e01a0f69f
ms.sourcegitcommit: 704d273485dcdc25c97a222bc0ef0695aad334d2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/28/2019
ms.locfileid: "770896"
---
# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a><span data-ttu-id="089e8-103">Microsoft Dynamics 365 for Field Service との統合</span><span class="sxs-lookup"><span data-stu-id="089e8-103">Integration with Microsoft Dynamics 365 for Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="089e8-104">Microsoft Dynamics 365 for Finance and Operations は、Finance and Operations および Microsoft Dynamics 365 for Field Service 間の業務プロセスの同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="089e8-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="089e8-105">統合シナリオは、業務プロセスの同期を有効にするため、拡張データ インテグレーター テンプレートおよび Common Data Service (CDS) を使用して構成します。</span><span class="sxs-lookup"><span data-stu-id="089e8-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>
<span data-ttu-id="089e8-106">標準テンプレートを使用してカスタム統合プロジェクトを作成し、追加の標準フィールドとカスタム フィールド、およびエンティティをマップして統合を調整して、特定のビジネス ニーズを満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="089e8-106">Standard templates can be used to create custom integration projects, where additional standard and custom fields and entities can be mapped to adjust the integration and meet specific business needs.</span></span> 

<span data-ttu-id="089e8-107">Field Service 統合は、既存の見込顧客の現金化機能の上に構築します。</span><span class="sxs-lookup"><span data-stu-id="089e8-107">The field service integration builds on top of the existing prospect-to-cash functionality.</span></span>

![Finance and Operations および Field Service 間の業務プロセスの同期](./media/field-service-integration.png)

<span data-ttu-id="089e8-109">Field Service および Finance and Operations の統合の第 1 のフェーズは、Field Service のワーク オーダーおよび契約を Finance and Operations で請求できるようにすることに重点を置いています。</span><span class="sxs-lookup"><span data-stu-id="089e8-109">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="089e8-110">Field Service でサポートされているフローが開始され、ワーク オーダーの情報が Finance and Operations に販売注文として同期されます。</span><span class="sxs-lookup"><span data-stu-id="089e8-110">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="089e8-111">Finance and Operations では、請求書ドキュメントを生成するために販売注文が請求されます。</span><span class="sxs-lookup"><span data-stu-id="089e8-111">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="089e8-112">さらに、Field Service 契約請求書からの情報は Finance and Operations に同期されます。</span><span class="sxs-lookup"><span data-stu-id="089e8-112">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="089e8-113">Microsoft Dynamics 365 データ インテグレーターは、カスタマイズ可能なプロジェクトを使用してデータを同期します。</span><span class="sxs-lookup"><span data-stu-id="089e8-113">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="089e8-114">標準テンプレートを使用してカスタム統合プロジェクトを作成し、追加の標準フィールドとカスタム フィールド、およびエンティティをマップして統合を調整し、特定の要件を満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="089e8-114">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="089e8-115">Field Service および Finance and Operations 統合の第 1 のフェーズは、次の項目の同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="089e8-115">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="089e8-116">製品タイプ情報を含む Field Service の製品への Finance and Operations の製品</span><span class="sxs-lookup"><span data-stu-id="089e8-116">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="089e8-117">Finance and Operations の販売注文への Field Service のワーク オーダー</span><span class="sxs-lookup"><span data-stu-id="089e8-117">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="089e8-118">Finance and Operations の自由書式の請求書への Field Service の契約の請求書</span><span class="sxs-lookup"><span data-stu-id="089e8-118">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

<span data-ttu-id="089e8-119">Field Service および Finance and Operations 間のワーク オーダーを同期する方法の例を表示するには、短い YouTube ビデオ [ワーク オーダーを Microsoft Dynamics 365 の統合に同期する方法](https://www.youtube.com/watch?v=46ylO7raZAo) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="089e8-119">To see an example of how you can synchronize a work order between Field Service and Finance and Operations, watch the short YouTube video [How to synchronize a work order with Microsoft Dynamics 365 Integration](https://www.youtube.com/watch?v=46ylO7raZAo).</span></span>

## <a name="integration-with-microsoft-dynamics-365-for-field-service-including-inventory-and-project-information"></a><span data-ttu-id="089e8-120">在庫およびプロジェクト情報を含む、Microsoft Dynamics 365 for Field Service との統合</span><span class="sxs-lookup"><span data-stu-id="089e8-120">Integration with Microsoft Dynamics 365 for Field Service, including inventory and project information</span></span>

<span data-ttu-id="089e8-121">この第 2 のフェーズの追加機能では、フィールド技術者に Finance and Operations からの在庫情報について洞察を与え、在庫レベルを更新し、材料を移動できるようにすることに重点を置いています。</span><span class="sxs-lookup"><span data-stu-id="089e8-121">The additional functionality in this second phase focused on giving field technicians insight about the inventory information from Finance and Operations, allowing them to update inventory levels and do material transfers.</span></span> <span data-ttu-id="089e8-122">さらに、販売品を設置またはサービスする会社は、プロジェクトからの統合により、販売およびサービスの全プロセスをより適切に管理および可視化することができます。</span><span class="sxs-lookup"><span data-stu-id="089e8-122">In addition, companies installing or servicing sold goods will benefit from better control and visibility to the full sales and service process with integration from projects.</span></span>

### <a name="functionality-includes-integration-of"></a><span data-ttu-id="089e8-123">機能には、以下の統合が含まれています:</span><span class="sxs-lookup"><span data-stu-id="089e8-123">Functionality includes integration of:</span></span>
- <span data-ttu-id="089e8-124">倉庫の情報</span><span class="sxs-lookup"><span data-stu-id="089e8-124">Warehouse information</span></span>
- <span data-ttu-id="089e8-125">手持在庫情報</span><span class="sxs-lookup"><span data-stu-id="089e8-125">On-hand inventory information</span></span>
- <span data-ttu-id="089e8-126">在庫移動</span><span class="sxs-lookup"><span data-stu-id="089e8-126">Inventory transfers</span></span>
- <span data-ttu-id="089e8-127">在庫調整</span><span class="sxs-lookup"><span data-stu-id="089e8-127">Inventory adjustments</span></span>
- <span data-ttu-id="089e8-128">Dynamics 365 for Field Service のワーク オーダーと接続した Dynamics 365 for Finance and Operations プロジェクト</span><span class="sxs-lookup"><span data-stu-id="089e8-128">Dynamics 365 for Finance and Operations projects connected with Dynamics 365 for Field Service work orders</span></span>
- <span data-ttu-id="089e8-129">Dynamics 365 for Finance and Operations プロジェクトへのリンクを含む Dynamics 365 for Field Serviceワーク オーダーは、このプロジェクト番号を Dynamics 365 for Finance and Operations 販売注文に適用して、プロジェクトからの請求を可能にします。</span><span class="sxs-lookup"><span data-stu-id="089e8-129">Dynamics 365 for Field Service work orders with link to Dynamics 365 for Finance and Operations projects, apply this project number to the Dynamics 365 for Finance and Operations sales order to allow invoicing from the project.</span></span> 

![Finance and Operations および Field Service 間の業務プロセスの同期](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-finance-and-operations-enables-synchronization-with-the-following-templates"></a><span data-ttu-id="089e8-131">Field Service および Finance and Operations 統合の第 2 のフェーズは、次のテンプレートとの同期を有効にします:</span><span class="sxs-lookup"><span data-stu-id="089e8-131">The second phase of the integration between Field Service and Finance and Operations enables synchronization with the following templates:</span></span>
- <span data-ttu-id="089e8-132">倉庫 (Finance and Operations から Field Service) - Finance and Operations から Field Service への倉庫 [高度なクエリ]</span><span class="sxs-lookup"><span data-stu-id="089e8-132">Warehouses (Fin and Ops to Field Service) - Warehouses from Finance and Operations to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="089e8-133">製品在庫 (Finance and Operations から Field Service) - Finance and Operations から Field Service への在庫レベル情報 [高度なクエリ]</span><span class="sxs-lookup"><span data-stu-id="089e8-133">Product Inventory (Fin and Ops to Field Service) - Inventory level information from Finance and Operations to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="089e8-134">在庫調整 (Field Service から Finance and Operations) - Field Service から Finance and Operations への在庫調整 [高度なクエリ]</span><span class="sxs-lookup"><span data-stu-id="089e8-134">Inventory Adjustment (Field Service to Fin and Ops) - Inventory adjustments from Field Service to Finance and Operations [Advanced Query]</span></span> 
- <span data-ttu-id="089e8-135">在庫移動 (Field Service から Finance and Operations) - Field Service から Finance and Operations への在庫移動 [高度なクエリ]</span><span class="sxs-lookup"><span data-stu-id="089e8-135">Inventory Transfers (Field Service to Fin and Ops) - Inventory transfers from Field Service to Finance and Operations [Advanced Query]</span></span> 
- <span data-ttu-id="089e8-136">プロジェクト (Finance and Operations から Field Service) - Finance and Operations から Field Service へのプロジェクト リスト [高度なクエリ]</span><span class="sxs-lookup"><span data-stu-id="089e8-136">Projects (Fin and Ops to Field Service) - Project list from Finance and Operations to Field Service</span></span> 
- <span data-ttu-id="089e8-137">プロジェクトのワーク オーダー (Field Service から Finance and Operations) - プロジェクトへのサポートを含む、Finance and Operations の販売注文に対する Field Service のワーク オーダー [高度なクエリ]</span><span class="sxs-lookup"><span data-stu-id="089e8-137">Work Orders with Project (Field Service to Fin and Ops) - Work orders in Field Service to Sales orders  in Finance and Operations, with support for Project [Advanced Query]</span></span> 
- <span data-ttu-id="089e8-138">Field Service 製品と在庫単位 (Finance and Operations から Sales) - Field Service への、在庫単位を含む Finance and Operations の「販売可能なリリース済製品」から Sales 「製品」</span><span class="sxs-lookup"><span data-stu-id="089e8-138">Field Service Products with Inventory unit (Fin and Ops to Sales) - Finance and Operations 'Sellable released products' to Sales 'Products' for Field Service, including Inventory unit</span></span> 

## <a name="system-requirements"></a><span data-ttu-id="089e8-139">システム要件</span><span class="sxs-lookup"><span data-stu-id="089e8-139">System requirements</span></span>

### <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="089e8-140">Finance and Operations のシステム要件</span><span class="sxs-lookup"><span data-stu-id="089e8-140">System requirements for Finance and Operations</span></span>
<span data-ttu-id="089e8-141">Field Service 統合は、次のバージョンがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="089e8-141">Field Service integration supports the following versions:</span></span>

- <span data-ttu-id="089e8-142">Dynamics 365 for Finance and Operations バージョン 8.1.2 (2018 年 12 月) は、2018 年 12 月にリリースされ、アプリケーション ビルド番号 8.1.195、プラットフォーム更新 22 (7.0.5095) となっています。</span><span class="sxs-lookup"><span data-stu-id="089e8-142">Dynamics 365 for Finance and Operations version 8.1.2 (December 2018) was released in December 2018 and has an application build number 8.1.195 with Platform Update 22 (7.0.5095).</span></span> 

### <a name="system-requirements-for-field-service"></a><span data-ttu-id="089e8-143">Field Service のシステム要件</span><span class="sxs-lookup"><span data-stu-id="089e8-143">System requirements for Field Service</span></span>
<span data-ttu-id="089e8-144">Field Service 統合ソリューションを使用するには、以下のコンポーネントをインストールする必要があります:</span><span class="sxs-lookup"><span data-stu-id="089e8-144">To use the Field Service integration solution, you must install the following components:</span></span>

- <span data-ttu-id="089e8-145">Field Service for Dynamics 365 (バージョン 8.2.0.286) または、Dynamics 365 9.1.x のそれ以降のバージョン - 2018 年 11 月リリース</span><span class="sxs-lookup"><span data-stu-id="089e8-145">Field Service for Dynamics 365 (version 8.2.0.286) or a later version on Dynamics 365 9.1.x - Released November 2018</span></span>
- <span data-ttu-id="089e8-146">Dynamics 365 バージョン 1.15.0.1 またはそれ以降のバージョンの見込顧客を現金化 (P2C) するソリューション。</span><span class="sxs-lookup"><span data-stu-id="089e8-146">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="089e8-147">このソリューションは、[AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3) からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="089e8-147">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="089e8-148">Dynamics 365 の「Field Service 統合、プロジェクトと在庫」ソリューション、バージョン 2.0.0.0 またはそれ以降のバージョン。</span><span class="sxs-lookup"><span data-stu-id="089e8-148">'Field Service Integration, Project and Inventory' solution for Dynamics 365, version 2.0.0.0 or a later version.</span></span> <span data-ttu-id="089e8-149">このソリューションは、[AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2) からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="089e8-149">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).</span></span>
