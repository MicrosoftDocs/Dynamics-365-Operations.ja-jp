---
title: サービスのための社内資産
description: このトピックでは、Microsoft Dtnamics 365 Field Service を使用して、顧客資産と社内資産の両方にサービスを提供する方法について説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 1e423199d0639db5e403e280880036b590149095
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172949"
---
# <a name="in-house-assets-for-servicing"></a><span data-ttu-id="f40b5-103">サービスのための社内資産</span><span class="sxs-lookup"><span data-stu-id="f40b5-103">In-house assets for servicing</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="f40b5-104">Microsoft Dynamics 365 Field Service は、顧客資産をサービスするように設計されています。</span><span class="sxs-lookup"><span data-stu-id="f40b5-104">Microsoft Dynamics 365 Field Service is designed to service customer assets.</span></span> <span data-ttu-id="f40b5-105">Dynamics 365 Supply Chain Management の資産管理は、社内資産を維持するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="f40b5-105">Asset management for Dynamics 365 Supply Chain Management is designed to maintain in-house assets.</span></span> <span data-ttu-id="f40b5-106">この 2 つのアプリを統合すると、Field Service を使用して顧客資産と社内資産の両方にサービスを提供できます。</span><span class="sxs-lookup"><span data-stu-id="f40b5-106">Integration of these two apps lets you use Field Service to service both customer assets and in-house assets.</span></span> <span data-ttu-id="f40b5-107">また、機能の場所または階層に基づいて資産を分類し、詳細レベルでサービスを追跡することもできます。</span><span class="sxs-lookup"><span data-stu-id="f40b5-107">You can also classify the assets, based on functional location or hierarchy, and track the servicing at a detailed level.</span></span>

<span data-ttu-id="f40b5-108">詳細については、[Dynamics 365 Field Service と Supply Chain Management の統合](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f40b5-108">For more information, see [Integrate Dynamics 365 Field Service and Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span></span>

## <a name="templates"></a><span data-ttu-id="f40b5-109">テンプレート</span><span class="sxs-lookup"><span data-stu-id="f40b5-109">Templates</span></span>

<span data-ttu-id="f40b5-110">社内資産には、次のテーブルに示すように、データの相互作用中に連携して作業するコア エンティティ マップのコレクションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f40b5-110">In-house-assets include a collection of core entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="f40b5-111">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="f40b5-111">Finance and Operations apps</span></span> | <span data-ttu-id="f40b5-112">Dynamics 365 のモデル駆動型アプリ</span><span class="sxs-lookup"><span data-stu-id="f40b5-112">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="f40b5-113">説明</span><span class="sxs-lookup"><span data-stu-id="f40b5-113">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="f40b5-114">資産管理資産のライフサイクル モデル</span><span class="sxs-lookup"><span data-stu-id="f40b5-114">Asset management asset lifecycle models</span></span> | <span data-ttu-id="f40b5-115">msdyn\_assetlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="f40b5-115">msdyn\_assetlifecyclemodels</span></span> | |
| <span data-ttu-id="f40b5-116">資産管理資産のライフサイクル状態</span><span class="sxs-lookup"><span data-stu-id="f40b5-116">Asset management asset lifecycle states</span></span> | <span data-ttu-id="f40b5-117">msdyn\_assetlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="f40b5-117">msdyn\_assetlifecyclestates</span></span> | |
| <span data-ttu-id="f40b5-118">資産管理資産</span><span class="sxs-lookup"><span data-stu-id="f40b5-118">Asset management assets</span></span> | <span data-ttu-id="f40b5-119">msdyn\_customerassets</span><span class="sxs-lookup"><span data-stu-id="f40b5-119">msdyn\_customerassets</span></span> | |
| <span data-ttu-id="f40b5-120">資産管理資産のタイプ</span><span class="sxs-lookup"><span data-stu-id="f40b5-120">Asset management asset types</span></span> | <span data-ttu-id="f40b5-121">msdyn\_customerassetcategories</span><span class="sxs-lookup"><span data-stu-id="f40b5-121">msdyn\_customerassetcategories</span></span> | |
| <span data-ttu-id="f40b5-122">資産管理機能の場所のライフサイクル モデル</span><span class="sxs-lookup"><span data-stu-id="f40b5-122">Asset management functional location lifecycle models</span></span> | <span data-ttu-id="f40b5-123">msdyn\_functionallocationlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="f40b5-123">msdyn\_functionallocationlifecyclemodels</span></span> | |
| <span data-ttu-id="f40b5-124">資産管理機能の場所のライフサイクル状態</span><span class="sxs-lookup"><span data-stu-id="f40b5-124">Asset management functional location lifecycle states</span></span> | <span data-ttu-id="f40b5-125">msdyn\_functionallocationlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="f40b5-125">msdyn\_functionallocationlifecyclestates</span></span> | |
| <span data-ttu-id="f40b5-126">資産管理機能の場所</span><span class="sxs-lookup"><span data-stu-id="f40b5-126">Asset management functional locations</span></span> | <span data-ttu-id="f40b5-127">msdyn\_functionallocations</span><span class="sxs-lookup"><span data-stu-id="f40b5-127">msdyn\_functionallocations</span></span> | |
| <span data-ttu-id="f40b5-128">資産管理機能の場所のタイプ</span><span class="sxs-lookup"><span data-stu-id="f40b5-128">Asset management functional location types</span></span> | <span data-ttu-id="f40b5-129">msdyn\_functionallocationtypes</span><span class="sxs-lookup"><span data-stu-id="f40b5-129">msdyn\_functionallocationtypes</span></span> | |
| <span data-ttu-id="f40b5-130">資産管理メーカー</span><span class="sxs-lookup"><span data-stu-id="f40b5-130">Asset management manufacturers</span></span> | <span data-ttu-id="f40b5-131">msdyn\_manufacturers</span><span class="sxs-lookup"><span data-stu-id="f40b5-131">msdyn\_manufacturers</span></span> | |
| <span data-ttu-id="f40b5-132">資産管理モデル</span><span class="sxs-lookup"><span data-stu-id="f40b5-132">Asset management models</span></span> | <span data-ttu-id="f40b5-133">msdyn\_models</span><span class="sxs-lookup"><span data-stu-id="f40b5-133">msdyn\_models</span></span> | |
| <span data-ttu-id="f40b5-134">資産管理の保証</span><span class="sxs-lookup"><span data-stu-id="f40b5-134">Asset management warranty</span></span> | <span data-ttu-id="f40b5-135">msdyn\_warranties</span><span class="sxs-lookup"><span data-stu-id="f40b5-135">msdyn\_warranties</span></span> | |

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [lifecycle models](includes/AssetManagementAssetLifecycleModels-msdyn-assetlifecyclemodels.md)]

[!include [lifecycle states](includes/AssetManagementAssetLifecycleStates-msdyn-assetlifecyclestates.md)]

[!include [assets](includes/AssetManagementAssets-msdyn-customerassets.md)]

[!include [asset types](includes/AssetManagementAssetTypes-msdyn-customerassetcategories.md)]

[!include [functional location lifecycle models](includes/AssetManagementFunctionalLocationLifecycleModels-msdyn-functionallocationlifecyclemodels.md)]

[!include [functional location lifecycle states](includes/AssetManagementFunctionalLocationLifecycleStates-msdyn-functionallocationlifecyclestates.md)]

[!include [functional locations](includes/AssetManagementFunctionalLocations-msdyn-functionallocations.md)]

[!include [functional location types](includes/AssetManagementFunctionalLocationTypes-msdyn-functionallocationtypes.md)]

[!include [manufacturers](includes/AssetManagementManufacturers-msdyn-manufacturers.md)]

[!include [models](includes/AssetManagementModels-msdyn-models.md)]

[!include [warranty](includes/AssetManagementWarranty-msdyn-warranties.md)]
