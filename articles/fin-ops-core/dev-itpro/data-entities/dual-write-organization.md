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
ms.openlocfilehash: fd159b38f69305dcaecb364ba0ccb3befabb3582
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182028"
---
## <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="0e115-103">Common Data Service の組織階層</span><span class="sxs-lookup"><span data-stu-id="0e115-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="0e115-104">Dynamics 365 Finance は財務システムであるため、*組織*は中核的な概念であり、システムの設定は組織階層の構成から始まります。</span><span class="sxs-lookup"><span data-stu-id="0e115-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="0e115-105">ビジネスの財務は、組織レベルおよび組織階層内のすべてのレベルで追跡できます。</span><span class="sxs-lookup"><span data-stu-id="0e115-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="0e115-106">Common Data Service は組織階層の概念はないが、総売上高など、いくつかの緩い概念はあります。</span><span class="sxs-lookup"><span data-stu-id="0e115-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="0e115-107">Common Data Service 統合の一環として、組織階層データ構造が Common Data Service に追加されます。</span><span class="sxs-lookup"><span data-stu-id="0e115-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="0e115-108">データ フロー</span><span class="sxs-lookup"><span data-stu-id="0e115-108">Data flow</span></span>

<span data-ttu-id="0e115-109">Finance and Operations アプリと Common Data Service を構成するビジネス エコシステムは、組織階層を持ち続けます。</span><span class="sxs-lookup"><span data-stu-id="0e115-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="0e115-110">この組織階層は Finance and Operations アプリに基づいて構築されていますが、情報と拡張目的のために Common Data Service で公開されています。</span><span class="sxs-lookup"><span data-stu-id="0e115-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="0e115-111">次の図は、Finance and Operations アプリから Common Data Service に一方向のデータ フローとして Common Data Service 内に公開される、組織階層の情報を示します。</span><span class="sxs-lookup"><span data-stu-id="0e115-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![アーキテクチャ イメージ](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="0e115-113">テンプレート</span><span class="sxs-lookup"><span data-stu-id="0e115-113">Templates</span></span>

<span data-ttu-id="0e115-114">組織階層のエンティティ マップは、Finance and Operations アプリから Common Data Service へのデータの一方向の同期に使用できます。</span><span class="sxs-lookup"><span data-stu-id="0e115-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="0e115-115">内部の組織階層の目的</span><span class="sxs-lookup"><span data-stu-id="0e115-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="0e115-116">このテンプレートは、Finance and Operations からその他の Dynamics 365 アプリへの組織階層目的エンティティの一方向の同期を提供します。</span><span class="sxs-lookup"><span data-stu-id="0e115-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="0e115-117">ソース フィールド</span><span class="sxs-lookup"><span data-stu-id="0e115-117">Source field</span></span> | <span data-ttu-id="0e115-118">タイプのマッピング</span><span class="sxs-lookup"><span data-stu-id="0e115-118">Map type</span></span> | <span data-ttu-id="0e115-119">出力先フィールド</span><span class="sxs-lookup"><span data-stu-id="0e115-119">Destination field</span></span>
---|---|---
<span data-ttu-id="0e115-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="0e115-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="0e115-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="0e115-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="0e115-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="0e115-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="0e115-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="0e115-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="0e115-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="0e115-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="0e115-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="0e115-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="0e115-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="0e115-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="0e115-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="0e115-127">msdyn\_immutable</span></span>
<span data-ttu-id="0e115-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="0e115-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="0e115-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="0e115-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="0e115-130">内部の組織階層タイプ</span><span class="sxs-lookup"><span data-stu-id="0e115-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="0e115-131">このテンプレートは、Finance and Operations からその他の Dynamics 365 アプリへの組織階層タイプ エンティティの一方向の同期を提供します。</span><span class="sxs-lookup"><span data-stu-id="0e115-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="0e115-132">ソース フィールド</span><span class="sxs-lookup"><span data-stu-id="0e115-132">Source field</span></span> | <span data-ttu-id="0e115-133">タイプのマッピング</span><span class="sxs-lookup"><span data-stu-id="0e115-133">Map type</span></span> | <span data-ttu-id="0e115-134">出力先フィールド</span><span class="sxs-lookup"><span data-stu-id="0e115-134">Destination field</span></span>
---|---|---
<span data-ttu-id="0e115-135">名前</span><span class="sxs-lookup"><span data-stu-id="0e115-135">NAME</span></span> | \> | <span data-ttu-id="0e115-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="0e115-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="0e115-137">内部の組織階層</span><span class="sxs-lookup"><span data-stu-id="0e115-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="0e115-138">このテンプレートは、Finance and Operations からその他の Dynamics 365 アプリへの組織階層の公開済みエンティティの一方向の同期を提供します。</span><span class="sxs-lookup"><span data-stu-id="0e115-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="0e115-139">ソース フィールド</span><span class="sxs-lookup"><span data-stu-id="0e115-139">Source field</span></span> | <span data-ttu-id="0e115-140">タイプのマッピング</span><span class="sxs-lookup"><span data-stu-id="0e115-140">Map type</span></span> | <span data-ttu-id="0e115-141">出力先フィールド</span><span class="sxs-lookup"><span data-stu-id="0e115-141">Destination field</span></span>
---|---|---
<span data-ttu-id="0e115-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="0e115-142">VALIDTO</span></span> | \> | <span data-ttu-id="0e115-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="0e115-143">msdyn\_validto</span></span>
<span data-ttu-id="0e115-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="0e115-144">VALIDFROM</span></span> | \> | <span data-ttu-id="0e115-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="0e115-145">msdyn\_validfrom</span></span>
<span data-ttu-id="0e115-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="0e115-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="0e115-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="0e115-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="0e115-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="0e115-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="0e115-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="0e115-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="0e115-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="0e115-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="0e115-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="0e115-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="0e115-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="0e115-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="0e115-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="0e115-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="0e115-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="0e115-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="0e115-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="0e115-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="0e115-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="0e115-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="0e115-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="0e115-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="0e115-158">内部組織</span><span class="sxs-lookup"><span data-stu-id="0e115-158">Internal Organization</span></span>

<span data-ttu-id="0e115-159">Common Data Service の内部組織情報は、**作業単位**と**法人エンティティ**の 2 つのエンティティから来ています。</span><span class="sxs-lookup"><span data-stu-id="0e115-159">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="0e115-160">作業単位</span><span class="sxs-lookup"><span data-stu-id="0e115-160">Operating unit</span></span>

<span data-ttu-id="0e115-161">ソース フィールド</span><span class="sxs-lookup"><span data-stu-id="0e115-161">Source field</span></span> | <span data-ttu-id="0e115-162">タイプのマッピング</span><span class="sxs-lookup"><span data-stu-id="0e115-162">Map type</span></span> | <span data-ttu-id="0e115-163">出力先フィールド</span><span class="sxs-lookup"><span data-stu-id="0e115-163">Destination field</span></span>
---|---|---
<span data-ttu-id="0e115-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="0e115-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="0e115-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="0e115-165">msdyn\_languageid</span></span>
<span data-ttu-id="0e115-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="0e115-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="0e115-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="0e115-167">msdyn\_namealias</span></span>
<span data-ttu-id="0e115-168">名前</span><span class="sxs-lookup"><span data-stu-id="0e115-168">NAME</span></span> | \> | <span data-ttu-id="0e115-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="0e115-169">msdyn\_name</span></span>
<span data-ttu-id="0e115-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="0e115-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="0e115-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="0e115-171">msdyn\_partynumber</span></span>
<span data-ttu-id="0e115-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="0e115-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="0e115-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="0e115-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="0e115-174">法人エンティティ</span><span class="sxs-lookup"><span data-stu-id="0e115-174">Legal entity</span></span>

<span data-ttu-id="0e115-175">ソース フィールド</span><span class="sxs-lookup"><span data-stu-id="0e115-175">Source field</span></span> | <span data-ttu-id="0e115-176">タイプのマッピング</span><span class="sxs-lookup"><span data-stu-id="0e115-176">Map type</span></span> | <span data-ttu-id="0e115-177">出力先フィールド</span><span class="sxs-lookup"><span data-stu-id="0e115-177">Destination field</span></span>
---|---|---
<span data-ttu-id="0e115-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="0e115-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="0e115-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="0e115-179">msdyn\_namealias</span></span>
<span data-ttu-id="0e115-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="0e115-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="0e115-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="0e115-181">msdyn\_languageid</span></span>
<span data-ttu-id="0e115-182">名前</span><span class="sxs-lookup"><span data-stu-id="0e115-182">NAME</span></span> | \> | <span data-ttu-id="0e115-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="0e115-183">msdyn\_name</span></span>
<span data-ttu-id="0e115-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="0e115-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="0e115-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="0e115-185">msdyn\_partynumber</span></span>
<span data-ttu-id="0e115-186">なし</span><span class="sxs-lookup"><span data-stu-id="0e115-186">none</span></span> | \>\> | <span data-ttu-id="0e115-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="0e115-187">msdyn\_type</span></span>
<span data-ttu-id="0e115-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="0e115-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="0e115-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="0e115-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="0e115-190">法人</span><span class="sxs-lookup"><span data-stu-id="0e115-190">Company</span></span>

<span data-ttu-id="0e115-191">Finance and Operations アプリとその他の Dynamics 365 アプリの間の法人 (会社) 情報の双方向同期を提供します。</span><span class="sxs-lookup"><span data-stu-id="0e115-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="0e115-192">ソース フィールド</span><span class="sxs-lookup"><span data-stu-id="0e115-192">Source field</span></span> | <span data-ttu-id="0e115-193">タイプのマッピング</span><span class="sxs-lookup"><span data-stu-id="0e115-193">Map type</span></span> | <span data-ttu-id="0e115-194">出力先フィールド</span><span class="sxs-lookup"><span data-stu-id="0e115-194">Destination field</span></span>
---|---|---
<span data-ttu-id="0e115-195">名前</span><span class="sxs-lookup"><span data-stu-id="0e115-195">NAME</span></span> | = | <span data-ttu-id="0e115-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="0e115-196">cdm\_name</span></span>
<span data-ttu-id="0e115-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="0e115-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="0e115-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="0e115-198">cdm\_companycode</span></span>
