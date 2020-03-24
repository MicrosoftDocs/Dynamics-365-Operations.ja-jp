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
ms.openlocfilehash: d931811e9fbea3c10f83b048a3c3fbeda5396d39
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112474"
---
# <a name="in-house-assets-for-servicing"></a><span data-ttu-id="6f012-103">サービスのための社内資産</span><span class="sxs-lookup"><span data-stu-id="6f012-103">In-house assets for servicing</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="6f012-104">Microsoft Dynamics 365 Field Service は、顧客資産をサービスするように設計されています。</span><span class="sxs-lookup"><span data-stu-id="6f012-104">Microsoft Dynamics 365 Field Service is designed to service customer assets.</span></span> <span data-ttu-id="6f012-105">Dynamics 365 Supply Chain Management の資産管理は、社内資産を維持するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="6f012-105">Asset management for Dynamics 365 Supply Chain Management is designed to maintain in-house assets.</span></span> <span data-ttu-id="6f012-106">この 2 つのアプリを統合すると、Field Service を使用して顧客資産と社内資産の両方にサービスを提供できます。</span><span class="sxs-lookup"><span data-stu-id="6f012-106">Integration of these two apps lets you use Field Service to service both customer assets and in-house assets.</span></span> <span data-ttu-id="6f012-107">また、機能の場所または階層に基づいて資産を分類し、詳細レベルでサービスを追跡することもできます。</span><span class="sxs-lookup"><span data-stu-id="6f012-107">You can also classify the assets, based on functional location or hierarchy, and track the servicing at a detailed level.</span></span>

<span data-ttu-id="6f012-108">詳細については、[Dynamics 365 Field Service と Supply Chain Management の統合](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f012-108">For more information, see [Integrate Dynamics 365 Field Service and Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span></span>

## <a name="templates"></a><span data-ttu-id="6f012-109">テンプレート</span><span class="sxs-lookup"><span data-stu-id="6f012-109">Templates</span></span>

<span data-ttu-id="6f012-110">社内資産には、次のテーブルに示すように、データの相互作用中に連携して作業するコア エンティティ マップのコレクションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6f012-110">In-house-assets include a collection of core entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="6f012-111">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="6f012-111">Finance and Operations apps</span></span> | <span data-ttu-id="6f012-112">Dynamics 365 のモデル駆動型アプリ</span><span class="sxs-lookup"><span data-stu-id="6f012-112">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="6f012-113">説明</span><span class="sxs-lookup"><span data-stu-id="6f012-113">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="6f012-114">資産管理資産のライフサイクル モデル</span><span class="sxs-lookup"><span data-stu-id="6f012-114">Asset management asset lifecycle models</span></span> | <span data-ttu-id="6f012-115">msdyn\_assetlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="6f012-115">msdyn\_assetlifecyclemodels</span></span> | |
| <span data-ttu-id="6f012-116">資産管理資産のライフサイクル状態</span><span class="sxs-lookup"><span data-stu-id="6f012-116">Asset management asset lifecycle states</span></span> | <span data-ttu-id="6f012-117">msdyn\_assetlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="6f012-117">msdyn\_assetlifecyclestates</span></span> | |
| <span data-ttu-id="6f012-118">資産管理資産</span><span class="sxs-lookup"><span data-stu-id="6f012-118">Asset management assets</span></span> | <span data-ttu-id="6f012-119">msdyn\_customerassets</span><span class="sxs-lookup"><span data-stu-id="6f012-119">msdyn\_customerassets</span></span> | |
| <span data-ttu-id="6f012-120">資産管理資産のタイプ</span><span class="sxs-lookup"><span data-stu-id="6f012-120">Asset management asset types</span></span> | <span data-ttu-id="6f012-121">msdyn\_customerassetcategories</span><span class="sxs-lookup"><span data-stu-id="6f012-121">msdyn\_customerassetcategories</span></span> | |
| <span data-ttu-id="6f012-122">資産管理機能の場所のライフサイクル モデル</span><span class="sxs-lookup"><span data-stu-id="6f012-122">Asset management functional location lifecycle models</span></span> | <span data-ttu-id="6f012-123">msdyn\_functionallocationlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="6f012-123">msdyn\_functionallocationlifecyclemodels</span></span> | |
| <span data-ttu-id="6f012-124">資産管理機能の場所のライフサイクル状態</span><span class="sxs-lookup"><span data-stu-id="6f012-124">Asset management functional location lifecycle states</span></span> | <span data-ttu-id="6f012-125">msdyn\_functionallocationlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="6f012-125">msdyn\_functionallocationlifecyclestates</span></span> | |
| <span data-ttu-id="6f012-126">資産管理機能の場所</span><span class="sxs-lookup"><span data-stu-id="6f012-126">Asset management functional locations</span></span> | <span data-ttu-id="6f012-127">msdyn\_functionallocations</span><span class="sxs-lookup"><span data-stu-id="6f012-127">msdyn\_functionallocations</span></span> | |
| <span data-ttu-id="6f012-128">資産管理機能の場所のタイプ</span><span class="sxs-lookup"><span data-stu-id="6f012-128">Asset management functional location types</span></span> | <span data-ttu-id="6f012-129">msdyn\_functionallocationtypes</span><span class="sxs-lookup"><span data-stu-id="6f012-129">msdyn\_functionallocationtypes</span></span> | |
| <span data-ttu-id="6f012-130">資産管理メーカー</span><span class="sxs-lookup"><span data-stu-id="6f012-130">Asset management manufacturers</span></span> | <span data-ttu-id="6f012-131">msdyn\_manufacturers</span><span class="sxs-lookup"><span data-stu-id="6f012-131">msdyn\_manufacturers</span></span> | |
| <span data-ttu-id="6f012-132">資産管理モデル</span><span class="sxs-lookup"><span data-stu-id="6f012-132">Asset management models</span></span> | <span data-ttu-id="6f012-133">msdyn\_models</span><span class="sxs-lookup"><span data-stu-id="6f012-133">msdyn\_models</span></span> | |
| <span data-ttu-id="6f012-134">資産管理の保証</span><span class="sxs-lookup"><span data-stu-id="6f012-134">Asset management warranty</span></span> | <span data-ttu-id="6f012-135">msdyn\_warranties</span><span class="sxs-lookup"><span data-stu-id="6f012-135">msdyn\_warranties</span></span> | |

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
