---
title: Dataverse の組織階層
description: このトピックでは、Finance and Operations アプリと Dataverse 間の組織データの統合について説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: f265d49a87383e2abf129b8d1d67567fc4b9e0de
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559582"
---
# <a name="organization-hierarchy-in-dataverse"></a><span data-ttu-id="319cf-103">Dataverse の組織階層</span><span class="sxs-lookup"><span data-stu-id="319cf-103">Organization hierarchy in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="319cf-104">Dynamics 365 Finance は財務システムであるため、*組織* は中核的な概念であり、システムの設定は組織階層の構成から始まります。</span><span class="sxs-lookup"><span data-stu-id="319cf-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="319cf-105">ビジネスの財務は、組織レベルおよび組織階層内のすべてのレベルで追跡できます。</span><span class="sxs-lookup"><span data-stu-id="319cf-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="319cf-106">Dataverse は組織階層の概念はないが、総売上高など、いくつかの緩い概念はあります。</span><span class="sxs-lookup"><span data-stu-id="319cf-106">Although Dataverse doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="319cf-107">Dataverse 統合の一環として、組織階層データ構造が Dataverse に追加されます。</span><span class="sxs-lookup"><span data-stu-id="319cf-107">As part of Dataverse integration, the organization hierarchy data structure is added to Dataverse.</span></span>

## <a name="data-flow"></a><span data-ttu-id="319cf-108">データ フロー</span><span class="sxs-lookup"><span data-stu-id="319cf-108">Data flow</span></span>

<span data-ttu-id="319cf-109">Finance and Operations アプリと Dataverse を構成するビジネス エコシステムは、組織階層を持ち続けます。</span><span class="sxs-lookup"><span data-stu-id="319cf-109">A business ecosystem that consists of Finance and Operations apps and Dataverse will continue to have an organization hierarchy.</span></span> <span data-ttu-id="319cf-110">この組織階層は Finance and Operations アプリに基づいて構築されていますが、情報と拡張目的のために Dataverse で公開されています。</span><span class="sxs-lookup"><span data-stu-id="319cf-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Dataverse for informational and extensibility purposes.</span></span> <span data-ttu-id="319cf-111">次の図は、Finance and Operations アプリから Dataverse に一方向のデータ フローとして Dataverse 内に公開される、組織階層の情報を示します。</span><span class="sxs-lookup"><span data-stu-id="319cf-111">The following illustration shows the organization hierarchy information that is exposed in Dataverse as a one-way data flow from Finance and Operations apps to Dataverse.</span></span>

![アーキテクチャ イメージ](media/dual-write-data-flow.png)

<span data-ttu-id="319cf-113">組織階層のテーブル マップは、Finance and Operations アプリから Dataverse へのデータの一方向の同期に使用できます。</span><span class="sxs-lookup"><span data-stu-id="319cf-113">Organization hierarchy table maps are available for one-way synchronization of data from Finance and Operations apps to Dataverse.</span></span>

## <a name="templates"></a><span data-ttu-id="319cf-114">テンプレート</span><span class="sxs-lookup"><span data-stu-id="319cf-114">Templates</span></span>

<span data-ttu-id="319cf-115">製品情報には、製品分析コードや追跡、保管分析コードなど、製品とその定義に関連するすべての情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="319cf-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="319cf-116">次のテーブルが示すように、製品と関連する情報を同期するためにテーブル マップのコレクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="319cf-116">As the following table shows, a collection of table maps is created to sync products and related information.</span></span>

<span data-ttu-id="319cf-117">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="319cf-117">Finance and Operations apps</span></span> | <span data-ttu-id="319cf-118">その他の Dynamics 365 アプリ</span><span class="sxs-lookup"><span data-stu-id="319cf-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="319cf-119">説明</span><span class="sxs-lookup"><span data-stu-id="319cf-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="319cf-120">組織階層の目的</span><span class="sxs-lookup"><span data-stu-id="319cf-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="319cf-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="319cf-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="319cf-122">このテンプレートでは、組織階層目的テーブルの一方向の同期を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="319cf-122">This template provides one-way synchronization of the Organization Hierarchy Purpose table.</span></span>
<span data-ttu-id="319cf-123">組織階層タイプ</span><span class="sxs-lookup"><span data-stu-id="319cf-123">Organization hierarchy type</span></span> | <span data-ttu-id="319cf-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="319cf-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="319cf-125">このテンプレートでは、組織階層タイプ テーブルの一方向の同期を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="319cf-125">This template provides one-way synchronization of the Organization Hierarchy Type table.</span></span>
<span data-ttu-id="319cf-126">組織階層 - 公開済み</span><span class="sxs-lookup"><span data-stu-id="319cf-126">Organization hierarchy - published</span></span> | <span data-ttu-id="319cf-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="319cf-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="319cf-128">このテンプレートでは、組織階層の公開済みテーブルの一方向の同期を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="319cf-128">This template provides one-way synchronization of the Organization Hierarchy Published table.</span></span>
<span data-ttu-id="319cf-129">作業単位</span><span class="sxs-lookup"><span data-stu-id="319cf-129">Operating unit</span></span> | <span data-ttu-id="319cf-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="319cf-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="319cf-131">法人</span><span class="sxs-lookup"><span data-stu-id="319cf-131">Legal entities</span></span> | <span data-ttu-id="319cf-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="319cf-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="319cf-133">法人</span><span class="sxs-lookup"><span data-stu-id="319cf-133">Legal entities</span></span> | <span data-ttu-id="319cf-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="319cf-134">cdm_companies</span></span> | <span data-ttu-id="319cf-135">法人 (会社) 情報の双方向の同期を提供します。</span><span class="sxs-lookup"><span data-stu-id="319cf-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="319cf-136">内部組織</span><span class="sxs-lookup"><span data-stu-id="319cf-136">Internal Organization</span></span>

<span data-ttu-id="319cf-137">Dataverse の内部組織情報は、**作業単位** と **法人エンティティ** の 2 つのテーブルから来ています。</span><span class="sxs-lookup"><span data-stu-id="319cf-137">Internal organization information in Dataverse comes from two tables, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]