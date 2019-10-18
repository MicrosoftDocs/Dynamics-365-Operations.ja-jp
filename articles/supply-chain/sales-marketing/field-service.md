---
title: Microsoft Dynamics 365 Field Service との統合の概要
description: このトピックでは、Microsoft Dynamics 365 Field Service との統合の概要を提供します。
author: ChristianRytt
manager: AnnBe
ms.date: 07/25/2019
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
ms.openlocfilehash: 2a5c3e49f09bf4f1f90449db10d439f563ecc2c0
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249845"
---
# <a name="integration-with-microsoft-dynamics-365-field-service-overview"></a><span data-ttu-id="737d1-103">Microsoft Dynamics 365 Field Service との統合の概要</span><span class="sxs-lookup"><span data-stu-id="737d1-103">Integration with Microsoft Dynamics 365 Field Service overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="737d1-104">Supply Chain Management により、Dynamics 365 Supply Chain Management および Dynamics 365 Field Service 間の業務プロセスの同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="737d1-104">Supply Chain Management enables synchronization of business processes between Dynamics 365 Supply Chain Management and Dynamics 365 Field Service.</span></span> <span data-ttu-id="737d1-105">統合シナリオは、業務プロセスの同期を有効にするため、拡張データ インテグレーター テンプレートおよび Common Data Service を使用して構成します。</span><span class="sxs-lookup"><span data-stu-id="737d1-105">The integration scenarios are configured by using extensible Data integrator templates and Common Data Service to enable the synchronization of business processes.</span></span>
<span data-ttu-id="737d1-106">標準テンプレートを使用してカスタム統合プロジェクトを作成し、追加の標準フィールドとカスタム フィールド、およびエンティティをマップして統合を調整して、特定のビジネス ニーズを満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="737d1-106">Standard templates can be used to create custom integration projects, where additional standard and custom fields and entities can be mapped to adjust the integration and meet specific business needs.</span></span> 

<span data-ttu-id="737d1-107">Field Service 統合は、既存の見込顧客の現金化機能の上に構築します。</span><span class="sxs-lookup"><span data-stu-id="737d1-107">The field service integration builds on top of the existing prospect-to-cash functionality.</span></span>

![Supply Chain Management および Field Service 間の業務プロセスの同期](./media/field-service-integration.png)

<span data-ttu-id="737d1-109">Field Service および Supply Chain Management の統合の第 1 のフェーズは、Field Service のワーク オーダーおよび契約を Supply Chain Management で請求できるようにすることに重点を置いています。</span><span class="sxs-lookup"><span data-stu-id="737d1-109">The first phase  of the integration between Field Service and Supply Chain Management is focused on enabling work orders and agreements in Field Service to be invoiced in Supply Chain Management.</span></span> <span data-ttu-id="737d1-110">Field Service でサポートされているフローが開始され、ワーク オーダーの情報が Supply Chain Management に販売注文として同期されます。</span><span class="sxs-lookup"><span data-stu-id="737d1-110">The supported flow starts in Field Service, where information from work orders is synchronized to Supply Chain Management as sales orders.</span></span> <span data-ttu-id="737d1-111">Supply Chain Management では、販売注文は請求書請求書ドキュメントを生成するために請求されます。</span><span class="sxs-lookup"><span data-stu-id="737d1-111">In Supply Chain Management, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="737d1-112">さらに、Field Service 契約請求書からの情報は Supply Chain Management に同期されます。</span><span class="sxs-lookup"><span data-stu-id="737d1-112">In addition, the information from Field Service agreement invoices is synchronized to Supply Chain Management.</span></span> <span data-ttu-id="737d1-113">Microsoft Dynamics 365 データ インテグレーターは、カスタマイズ可能なプロジェクトを使用してデータを同期します。</span><span class="sxs-lookup"><span data-stu-id="737d1-113">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="737d1-114">標準テンプレートを使用してカスタム統合プロジェクトを作成し、追加の標準フィールドとカスタム フィールド、およびエンティティをマップして統合を調整し、特定の要件を満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="737d1-114">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="737d1-115">Field Service および Supply Chain Management 統合の第 1 のフェーズは、次の項目の同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="737d1-115">The first phase of the integration between Field Service and Supply Chain Management enables synchronization of the following items:</span></span>

- [<span data-ttu-id="737d1-116">製品タイプ情報を含む Field Service の製品への Supply Chain Management の製品</span><span class="sxs-lookup"><span data-stu-id="737d1-116">Products in Supply Chain Management to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="737d1-117">Field Service のワーク オーダーから Supply Chain Management の販売注文</span><span class="sxs-lookup"><span data-stu-id="737d1-117">Work orders in Field Service to sales orders in Supply Chain Management</span></span>](field-service-work-order.md)
- [<span data-ttu-id="737d1-118">Field Service の請求書から Supply Chain Management の自由書式の請求書</span><span class="sxs-lookup"><span data-stu-id="737d1-118">Invoices in Field Service to free text invoices in Supply Chain Management</span></span>](field-service-invoice.md)

<span data-ttu-id="737d1-119">Field Service および Supply Chain Management 間のワーク オーダーを同期する方法の例を表示するには、短い YouTube ビデオ [ワーク オーダーを Microsoft Dynamics 365 の統合に同期する方法](https://www.youtube.com/watch?v=46ylO7raZAo) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="737d1-119">To see an example of how you can synchronize a work order between Field Service and Supply Chain Management, watch the short YouTube video [How to synchronize a work order with Microsoft Dynamics 365 Integration](https://www.youtube.com/watch?v=46ylO7raZAo).</span></span>

## <a name="integration-with-field-service-including-inventory-and-project-information"></a><span data-ttu-id="737d1-120">在庫およびプロジェクト情報を含む、Field Service との統合</span><span class="sxs-lookup"><span data-stu-id="737d1-120">Integration with Field Service, including inventory and project information</span></span>

<span data-ttu-id="737d1-121">この第 2 のフェーズの追加機能では、フィールド技術者に Supply Chain Management からの在庫情報について洞察を与え、在庫レベルを更新し、材料を移動できるようにすることに重点を置いています。</span><span class="sxs-lookup"><span data-stu-id="737d1-121">The additional functionality in this second phase focused on giving field technicians insight about the inventory information from Supply Chain Management, allowing them to update inventory levels and do material transfers.</span></span> <span data-ttu-id="737d1-122">さらに、販売品を設置またはサービスする会社は、プロジェクトからの統合により、販売およびサービスの全プロセスをより適切に管理および可視化することができます。</span><span class="sxs-lookup"><span data-stu-id="737d1-122">In addition, companies installing or servicing sold goods will benefit from better control and visibility to the full sales and service process with integration from projects.</span></span>

### <a name="functionality-includes-integration-of"></a><span data-ttu-id="737d1-123">機能には、以下の統合が含まれています:</span><span class="sxs-lookup"><span data-stu-id="737d1-123">Functionality includes integration of:</span></span>
- <span data-ttu-id="737d1-124">倉庫の情報</span><span class="sxs-lookup"><span data-stu-id="737d1-124">Warehouse information</span></span>
- <span data-ttu-id="737d1-125">手持在庫情報</span><span class="sxs-lookup"><span data-stu-id="737d1-125">On-hand inventory information</span></span>
- <span data-ttu-id="737d1-126">在庫移動</span><span class="sxs-lookup"><span data-stu-id="737d1-126">Inventory transfers</span></span>
- <span data-ttu-id="737d1-127">在庫調整</span><span class="sxs-lookup"><span data-stu-id="737d1-127">Inventory adjustments</span></span>
- <span data-ttu-id="737d1-128">Dynamics 365 Field Service ワーク オーダーに関連付けられた Supply Chain Management のプロジェクト</span><span class="sxs-lookup"><span data-stu-id="737d1-128">Supply Chain Management projects connected with Dynamics 365 Field Service work orders</span></span>
- <span data-ttu-id="737d1-129">Supply Chain Management プロジェクトへのリンクを含む Dynamics 365 Field Service ワーク オーダーは、このプロジェクト番号を販売注文に適用して、プロジェクトからの請求を可能にします。</span><span class="sxs-lookup"><span data-stu-id="737d1-129">Dynamics 365 Field Service work orders with link to Supply Chain Management projects, apply this project number to the sales order to allow invoicing from the project.</span></span> 

![Supply Chain Management および Field Service 間の業務プロセスの同期](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-supply-chain-management-enables-synchronization-with-the-following-templates"></a><span data-ttu-id="737d1-131">Field Service および Supply Chain Management 統合の第 2 のフェーズは、次のテンプレートとの同期を有効にします:</span><span class="sxs-lookup"><span data-stu-id="737d1-131">The second phase of the integration between Field Service and Supply Chain Management enables synchronization with the following templates:</span></span>
- <span data-ttu-id="737d1-132">倉庫 (Supply Chain Management から Field Service) - Supply Chain Management の倉庫から Field Service [高度なクエリ]</span><span class="sxs-lookup"><span data-stu-id="737d1-132">Warehouses (Supply Chain Management to Field Service) - Warehouses from Supply Chain Management to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="737d1-133">製品在庫 (Supply Chain Management から Field Service) - Supply Chain Management から Field Service への在庫レベル情報 [高度なクエリ]</span><span class="sxs-lookup"><span data-stu-id="737d1-133">Product Inventory (Supply Chain Management to Field Service) - Inventory level information from Supply Chain Management to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="737d1-134">在庫調整 (Field Service から Supply Chain Management) - Field Service から Supply Chain Management への在庫調整 [高度なクエリ]</span><span class="sxs-lookup"><span data-stu-id="737d1-134">Inventory Adjustment (Field Service to Supply Chain Management) - Inventory adjustments from Field Service to Supply Chain Management [Advanced Query]</span></span> 
- <span data-ttu-id="737d1-135">在庫振替 (Field Service から Supply Chain Management) - Field Service から Supply Chain Management への在庫振替 [高度なクエリ]</span><span class="sxs-lookup"><span data-stu-id="737d1-135">Inventory Transfers (Field Service to Supply Chain Management) - Inventory transfers from Field Service to Supply Chain Management [Advanced Query]</span></span> 
- <span data-ttu-id="737d1-136">プロジェクト (Supply Chain Management から Field Service) - Supply Chain Management から Field Service へのプロジェクト リスト</span><span class="sxs-lookup"><span data-stu-id="737d1-136">Projects (Supply Chain Management to Field Service) - Project list from Supply Chain Management to Field Service</span></span> 
- <span data-ttu-id="737d1-137">プロジェクトのワーク オーダー (Field Service から Supply Chain Management) - プロジェクトへのサポートを含む、Supply Chain Management の販売注文に対する Field Service のワーク オーダー [高度なクエリ]</span><span class="sxs-lookup"><span data-stu-id="737d1-137">Work Orders with Project (Field Service to Supply Chain Management) - Work orders in Field Service to Sales orders  in Supply Chain Management, with support for Project [Advanced Query]</span></span> 
- <span data-ttu-id="737d1-138">Field Service 製品と在庫単位 (Supply Chain Management から Sales) - Field Service への、在庫単位を含む Supply Chain Management の「販売可能なリリース済製品」から Sales 「製品」</span><span class="sxs-lookup"><span data-stu-id="737d1-138">Field Service Products with Inventory unit (Supply Chain Management to Sales) - Supply Chain Management 'Sellable released products' to Sales 'Products' for Field Service, including Inventory unit</span></span> 

## <a name="system-requirements"></a><span data-ttu-id="737d1-139">システム要件</span><span class="sxs-lookup"><span data-stu-id="737d1-139">System requirements</span></span>

### <a name="system-requirements-for-supply-chain-management"></a><span data-ttu-id="737d1-140">Supply Chain Management のシステム要件</span><span class="sxs-lookup"><span data-stu-id="737d1-140">System requirements for Supply Chain Management</span></span>
<span data-ttu-id="737d1-141">Field Service 統合は、次のバージョンがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="737d1-141">Field Service integration supports the following versions:</span></span>

- <span data-ttu-id="737d1-142">Dynamics 365 for Finance and Operations バージョン 8.1.2 (2018 年 12 月) は、2018 年 12 月にリリースされ、アプリケーション ビルド番号 8.1.195、プラットフォーム更新 22 (7.0.5095) となっています。</span><span class="sxs-lookup"><span data-stu-id="737d1-142">Dynamics 365 for Finance and Operations version 8.1.2 (December 2018) was released in December 2018 and has an application build number 8.1.195 with Platform update 22 (7.0.5095).</span></span> 

### <a name="system-requirements-for-field-service"></a><span data-ttu-id="737d1-143">Field Service のシステム要件</span><span class="sxs-lookup"><span data-stu-id="737d1-143">System requirements for Field Service</span></span>
<span data-ttu-id="737d1-144">Field Service 統合ソリューションを使用するには、以下のコンポーネントをインストールする必要があります:</span><span class="sxs-lookup"><span data-stu-id="737d1-144">To use the Field Service integration solution, you must install the following components:</span></span>

- <span data-ttu-id="737d1-145">Field Service (バージョン 8.2.0.286) または、Dynamics 365 9.1.x のそれ以降のバージョン - 2018 年 11 月リリース</span><span class="sxs-lookup"><span data-stu-id="737d1-145">Field Service (version 8.2.0.286) or a later version on Dynamics 365 9.1.x - Released November 2018</span></span>
- <span data-ttu-id="737d1-146">Dynamics 365 バージョン 1.15.0.1 またはそれ以降のバージョンの見込顧客を現金化 (P2C) するソリューション。</span><span class="sxs-lookup"><span data-stu-id="737d1-146">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="737d1-147">このソリューションは、[AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3) からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="737d1-147">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="737d1-148">Dynamics 365 の「Field Service 統合、プロジェクトと在庫」ソリューション、バージョン 2.0.0.0 またはそれ以降のバージョン。</span><span class="sxs-lookup"><span data-stu-id="737d1-148">'Field Service Integration, Project and Inventory' solution for Dynamics 365, version 2.0.0.0 or a later version.</span></span> <span data-ttu-id="737d1-149">このソリューションは、[AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2) からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="737d1-149">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).</span></span>
