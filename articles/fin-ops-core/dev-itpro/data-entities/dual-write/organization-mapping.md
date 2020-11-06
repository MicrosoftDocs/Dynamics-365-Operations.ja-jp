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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: f502519ba419cb8fa322eb1d22f06d2b805f5f05
ms.sourcegitcommit: afc43699c0edc4ff2be310cb37add2ab586b64c0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/14/2020
ms.locfileid: "4000737"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="f1e58-103">Common Data Service の組織階層</span><span class="sxs-lookup"><span data-stu-id="f1e58-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f1e58-104">Dynamics 365 Finance は財務システムであるため、 *組織* は中核的な概念であり、システムの設定は組織階層の構成から始まります。</span><span class="sxs-lookup"><span data-stu-id="f1e58-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="f1e58-105">ビジネスの財務は、組織レベルおよび組織階層内のすべてのレベルで追跡できます。</span><span class="sxs-lookup"><span data-stu-id="f1e58-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="f1e58-106">Common Data Service は組織階層の概念はないが、総売上高など、いくつかの緩い概念はあります。</span><span class="sxs-lookup"><span data-stu-id="f1e58-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="f1e58-107">Common Data Service 統合の一環として、組織階層データ構造が Common Data Service に追加されます。</span><span class="sxs-lookup"><span data-stu-id="f1e58-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="f1e58-108">データ フロー</span><span class="sxs-lookup"><span data-stu-id="f1e58-108">Data flow</span></span>

<span data-ttu-id="f1e58-109">Finance and Operations アプリと Common Data Service を構成するビジネス エコシステムは、組織階層を持ち続けます。</span><span class="sxs-lookup"><span data-stu-id="f1e58-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="f1e58-110">この組織階層は Finance and Operations アプリに基づいて構築されていますが、情報と拡張目的のために Common Data Service で公開されています。</span><span class="sxs-lookup"><span data-stu-id="f1e58-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="f1e58-111">次の図は、Finance and Operations アプリから Common Data Service に一方向のデータ フローとして Common Data Service 内に公開される、組織階層の情報を示します。</span><span class="sxs-lookup"><span data-stu-id="f1e58-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![アーキテクチャ イメージ](media/dual-write-data-flow.png)

<span data-ttu-id="f1e58-113">組織階層のエンティティ マップは、Finance and Operations アプリから Common Data Service へのデータの一方向の同期に使用できます。</span><span class="sxs-lookup"><span data-stu-id="f1e58-113">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

## <a name="templates"></a><span data-ttu-id="f1e58-114">テンプレート</span><span class="sxs-lookup"><span data-stu-id="f1e58-114">Templates</span></span>

<span data-ttu-id="f1e58-115">製品情報には、製品分析コードや追跡、保管分析コードなど、製品とその定義に関連するすべての情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f1e58-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="f1e58-116">次の表が示すように、製品と関連する情報を同期するためにエンティティ マップのコレクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="f1e58-116">As the following table shows, a collection of entity maps is created to sync products and related information.</span></span>

<span data-ttu-id="f1e58-117">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="f1e58-117">Finance and Operations apps</span></span> | <span data-ttu-id="f1e58-118">その他の Dynamics 365 アプリ</span><span class="sxs-lookup"><span data-stu-id="f1e58-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="f1e58-119">説明</span><span class="sxs-lookup"><span data-stu-id="f1e58-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="f1e58-120">組織階層の目的</span><span class="sxs-lookup"><span data-stu-id="f1e58-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="f1e58-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="f1e58-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="f1e58-122">このテンプレートでは、組織階層目的エンティティの一方向の同期を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f1e58-122">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="f1e58-123">組織階層タイプ</span><span class="sxs-lookup"><span data-stu-id="f1e58-123">Organization hierarchy type</span></span> | <span data-ttu-id="f1e58-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="f1e58-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="f1e58-125">このテンプレートでは、組織階層タイプ エンティティの一方向の同期を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f1e58-125">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="f1e58-126">組織階層 - 公開済</span><span class="sxs-lookup"><span data-stu-id="f1e58-126">Organization hierarchy - published</span></span> | <span data-ttu-id="f1e58-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="f1e58-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="f1e58-128">このテンプレートでは、組織階層の公開済みエンティティの一方向の同期を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f1e58-128">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="f1e58-129">作業単位</span><span class="sxs-lookup"><span data-stu-id="f1e58-129">Operating unit</span></span> | <span data-ttu-id="f1e58-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="f1e58-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="f1e58-131">法人</span><span class="sxs-lookup"><span data-stu-id="f1e58-131">Legal entities</span></span> | <span data-ttu-id="f1e58-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="f1e58-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="f1e58-133">法人</span><span class="sxs-lookup"><span data-stu-id="f1e58-133">Legal entities</span></span> | <span data-ttu-id="f1e58-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="f1e58-134">cdm_companies</span></span> | <span data-ttu-id="f1e58-135">法人 (会社) 情報の双方向の同期を提供します。</span><span class="sxs-lookup"><span data-stu-id="f1e58-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="f1e58-136">内部組織</span><span class="sxs-lookup"><span data-stu-id="f1e58-136">Internal Organization</span></span>

<span data-ttu-id="f1e58-137">Common Data Service の内部組織情報は、 **作業単位** と **法人エンティティ** の 2 つのエンティティから来ています。</span><span class="sxs-lookup"><span data-stu-id="f1e58-137">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
