---
title: Common Data Service の組織階層
description: このトピックでは、Finance and Operations アプリと Common Data Service 間の組織データの統合について説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: fbf7cc33d12fb54d2ff02acc46ba2e284b2a2b3f
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019878"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="0825f-103">Common Data Service の組織階層</span><span class="sxs-lookup"><span data-stu-id="0825f-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="0825f-104">Dynamics 365 Finance は財務システムであるため、*組織*は中核的な概念であり、システムの設定は組織階層の構成から始まります。</span><span class="sxs-lookup"><span data-stu-id="0825f-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="0825f-105">ビジネスの財務は、組織レベルおよび組織階層内のすべてのレベルで追跡できます。</span><span class="sxs-lookup"><span data-stu-id="0825f-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="0825f-106">Common Data Service は組織階層の概念はないが、総売上高など、いくつかの緩い概念はあります。</span><span class="sxs-lookup"><span data-stu-id="0825f-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="0825f-107">Common Data Service 統合の一環として、組織階層データ構造が Common Data Service に追加されます。</span><span class="sxs-lookup"><span data-stu-id="0825f-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="0825f-108">データ フロー</span><span class="sxs-lookup"><span data-stu-id="0825f-108">Data flow</span></span>

<span data-ttu-id="0825f-109">Finance and Operations アプリと Common Data Service を構成するビジネス エコシステムは、組織階層を持ち続けます。</span><span class="sxs-lookup"><span data-stu-id="0825f-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="0825f-110">この組織階層は Finance and Operations アプリに基づいて構築されていますが、情報と拡張目的のために Common Data Service で公開されています。</span><span class="sxs-lookup"><span data-stu-id="0825f-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="0825f-111">次の図は、Finance and Operations アプリから Common Data Service に一方向のデータ フローとして Common Data Service 内に公開される、組織階層の情報を示します。</span><span class="sxs-lookup"><span data-stu-id="0825f-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![アーキテクチャ イメージ](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="0825f-113">テンプレート</span><span class="sxs-lookup"><span data-stu-id="0825f-113">Templates</span></span>

<span data-ttu-id="0825f-114">組織階層のエンティティ マップは、Finance and Operations アプリから Common Data Service へのデータの一方向の同期に使用できます。</span><span class="sxs-lookup"><span data-stu-id="0825f-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

## <a name="templates"></a><span data-ttu-id="0825f-115">テンプレート</span><span class="sxs-lookup"><span data-stu-id="0825f-115">Templates</span></span>

<span data-ttu-id="0825f-116">製品情報には、製品分析コードや追跡、保管分析コードなど、製品とその定義に関連するすべての情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0825f-116">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="0825f-117">次の表が示すように、製品と関連する情報を同期するためにエンティティ マップのコレクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="0825f-117">As the following table shows, a collection of entity maps is created to sync products and related information.</span></span>

<span data-ttu-id="0825f-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0825f-118">Finance and Operations</span></span> | <span data-ttu-id="0825f-119">その他の Dynamics 365 アプリ</span><span class="sxs-lookup"><span data-stu-id="0825f-119">Other Dynamics 365 apps</span></span> | <span data-ttu-id="0825f-120">説明</span><span class="sxs-lookup"><span data-stu-id="0825f-120">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="0825f-121">組織階層の目的</span><span class="sxs-lookup"><span data-stu-id="0825f-121">Organization hierarchy purposes</span></span> | <span data-ttu-id="0825f-122">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="0825f-122">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="0825f-123">このテンプレートでは、組織階層目的エンティティの一方向の同期を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="0825f-123">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="0825f-124">組織階層タイプ</span><span class="sxs-lookup"><span data-stu-id="0825f-124">Organization hierarchy type</span></span> | <span data-ttu-id="0825f-125">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="0825f-125">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="0825f-126">このテンプレートでは、組織階層タイプ エンティティの一方向の同期を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="0825f-126">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="0825f-127">組織階層 - 公開済</span><span class="sxs-lookup"><span data-stu-id="0825f-127">Organization hierarchy - published</span></span> | <span data-ttu-id="0825f-128">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="0825f-128">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="0825f-129">このテンプレートでは、組織階層の公開済みエンティティの一方向の同期を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="0825f-129">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="0825f-130">作業単位</span><span class="sxs-lookup"><span data-stu-id="0825f-130">Operating unit</span></span> | <span data-ttu-id="0825f-131">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="0825f-131">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="0825f-132">法人</span><span class="sxs-lookup"><span data-stu-id="0825f-132">Legal entities</span></span> | <span data-ttu-id="0825f-133">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="0825f-133">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="0825f-134">法人</span><span class="sxs-lookup"><span data-stu-id="0825f-134">Legal entities</span></span> | <span data-ttu-id="0825f-135">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="0825f-135">cdm_companies</span></span> | <span data-ttu-id="0825f-136">法人 (会社) 情報の双方向の同期を提供します。</span><span class="sxs-lookup"><span data-stu-id="0825f-136">Provides bidirectional synchronization of legal entity (company) information.</span></span>


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="0825f-137">内部組織</span><span class="sxs-lookup"><span data-stu-id="0825f-137">Internal Organization</span></span>

<span data-ttu-id="0825f-138">Common Data Service の内部組織情報は、**作業単位**と**法人エンティティ**の 2 つのエンティティから来ています。</span><span class="sxs-lookup"><span data-stu-id="0825f-138">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]

