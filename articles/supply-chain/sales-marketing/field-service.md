---
title: "Microsoft Dynamics 365 for Field Service との統合"
description: "このトピックでは、Microsoft Dynamics 365 for Field Service との統合の概要を示します。"
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 841ea53f754f61c2930e77fdafc85eac72f47d7a
ms.openlocfilehash: 29e5748a1e1c381febae80d02b4ac311c3f0008e
ms.contentlocale: ja-jp
ms.lasthandoff: 07/21/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a><span data-ttu-id="36405-103">Microsoft Dynamics 365 for Field Service との統合</span><span class="sxs-lookup"><span data-stu-id="36405-103">Integration with Microsoft Dynamics 365 for Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="36405-104">Microsoft Dynamics 365 for Finance and Operations は、Finance and Operations および Microsoft Dynamics 365 for Field Service 間の業務プロセスの同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="36405-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="36405-105">統合シナリオは、業務プロセスの同期を有効にするため、拡張データ インテグレーター テンプレートおよび Common Data Service (CD) を使用して構成します。</span><span class="sxs-lookup"><span data-stu-id="36405-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>

<span data-ttu-id="36405-106">[![Finance and Operations および Field Service 間の業務プロセスの同期](./media/field-service-integration.png)](./media/field-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="36405-106">[![Synchronization of business processes between Finance and Operations and Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span></span>

<span data-ttu-id="36405-107">Field Service および Finance and Operations の統合の第 1 のフェーズは、Field Service のワーク オーダーおよび契約を Finance and Operations で請求できるようにすることに重点を置いています。</span><span class="sxs-lookup"><span data-stu-id="36405-107">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="36405-108">Field Service でサポートされているフローが開始され、ワーク オーダーの情報が Finance and Operations に販売注文として同期されます。</span><span class="sxs-lookup"><span data-stu-id="36405-108">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="36405-109">Finance and Operations では、請求書ドキュメントを生成するために販売注文が請求されます。</span><span class="sxs-lookup"><span data-stu-id="36405-109">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="36405-110">さらに、Field Service 契約請求書からの情報は Finance and Operations に同期されます。</span><span class="sxs-lookup"><span data-stu-id="36405-110">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="36405-111">Microsoft Dynamics 365 データ インテグレーターは、カスタマイズ可能なプロジェクトを使用してデータを同期します。</span><span class="sxs-lookup"><span data-stu-id="36405-111">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="36405-112">標準テンプレートを使用してカスタム統合プロジェクトを作成し、追加の標準フィールドとカスタム フィールド、およびエンティティをマップして統合を調整し、特定の要件を満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="36405-112">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="36405-113">Field Service および Finance and Operations 統合の第 1 のフェーズは、次の項目の同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="36405-113">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="36405-114">製品タイプ情報を含む Field Service の製品への Finance and Operations の製品</span><span class="sxs-lookup"><span data-stu-id="36405-114">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="36405-115">Finance and Operations の販売注文への Field Service のワーク オーダー</span><span class="sxs-lookup"><span data-stu-id="36405-115">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="36405-116">Finance and Operations の自由書式の請求書への Field Service の契約の請求書</span><span class="sxs-lookup"><span data-stu-id="36405-116">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

<span data-ttu-id="36405-117">Field Service および Finance and Operations 間のワーク オーダーを同期する方法の例を表示するには、短い YouTube ビデオ [Dynamics 365 for Field Service および Finance and Operations 間のワーク オーダーを同期する](https://www.youtube.com/watch?v=hAB4TDVMjxU)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="36405-117">To see an example of how you can synchronize a work order between Field Service and Finance and Operations, watch the short YouTube video [Synchronize a work order between Dynamics 365 for Field Service and Finance and Operations](https://www.youtube.com/watch?v=hAB4TDVMjxU).</span></span>

[![](https://img.youtube.com/vi/hAB4TDVMjxU/0.jpg)](https://www.youtube.com/watch?v=hAB4TDVMjxU)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="36405-118">Finance and Operations のシステム要件</span><span class="sxs-lookup"><span data-stu-id="36405-118">System requirements for Finance and Operations</span></span>
<span data-ttu-id="36405-119">Field Service 統合は、次のバージョンがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="36405-119">Field Service integration supports the following versions:</span></span>

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a><span data-ttu-id="36405-120">Dynamics 365 for Finance and Operations バージョン 8.0 (2018 年 4 月) またはそれ以降</span><span class="sxs-lookup"><span data-stu-id="36405-120">Dynamics 365 for Finance and Operations version 8.0 (April 2018) or later</span></span>

- <span data-ttu-id="36405-121">Dynamics 365 for Finance and Operations バージョン 8.0 (2018 年 4 月) は 2018 年 4 月にリリースされ、アプリケーション ビルド番号 8.0.30.8020、プラットフォーム更新プログラム 15 (7.0.4841.35234) となっています。</span><span class="sxs-lookup"><span data-stu-id="36405-121">Dynamics 365 for Finance and Operations version 8.0 (April 2018) was released in April 2018 and has an application build number 8.0.30.8020 with Platform Update 15 (7.0.4841.35234).</span></span> 

## <a name="system-requirements-for-field-service"></a><span data-ttu-id="36405-122">Field Service のシステム要件</span><span class="sxs-lookup"><span data-stu-id="36405-122">System requirements for Field Service</span></span>
<span data-ttu-id="36405-123">Field Service 統合ソリューションを使用するには、以下のコンポーネントをインストールする必要があります:</span><span class="sxs-lookup"><span data-stu-id="36405-123">To use the Field Service integration solution, you must install the following components:</span></span>

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a><span data-ttu-id="36405-124">Microsoft Dynamics 365 for Field Service 9.0 またはそれ以降</span><span class="sxs-lookup"><span data-stu-id="36405-124">Microsoft Dynamics 365 for Field Service 9.0 or later</span></span>

- <span data-ttu-id="36405-125">Dynamics 365 for Field Service バージョン 1612 (9.0.1.733) (DB 9.0.1.733) オンラインまたはそれ以降のバージョン。</span><span class="sxs-lookup"><span data-stu-id="36405-125">Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online or a later version.</span></span>
- <span data-ttu-id="36405-126">Dynamics 365 for Sales バージョン 1.15.0.1 またはそれ以降のバージョンの見込顧客を現金化 (P2C) するソリューション。</span><span class="sxs-lookup"><span data-stu-id="36405-126">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="36405-127">このソリューションは、[AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3) からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="36405-127">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="36405-128">Dynamics 365 バージョン 1.0.0.0 またはそれ以降のバージョンの Field Service 統合ソリューション。</span><span class="sxs-lookup"><span data-stu-id="36405-128">Field Service integration solution for Dynamics 365, version 1.0.0.0 or a later version.</span></span> <span data-ttu-id="36405-129">このソリューションは、[AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration) からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="36405-129">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).</span></span>

