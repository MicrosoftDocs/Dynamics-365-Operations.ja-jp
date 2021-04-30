---
title: Dynamics 365 グローバリゼーション サービス
description: このトピックでは、Microsoft Dynamics 365 グローバリゼーション サービスの概要を示します。
author: JaneA07
manager: AnnBe
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 8c6f3b7fb4dec0dffe55014e9e2d60620dc3b193
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893051"
---
# <a name="dynamics-365-globalization-services"></a><span data-ttu-id="f6713-103">Dynamics 365 グローバリゼーション サービス</span><span class="sxs-lookup"><span data-stu-id="f6713-103">Dynamics 365 globalization services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6713-104">次のグローバリゼーション サービスは、一部の Microsoft Dynamics 365 オンライン サービスに存在する機能を拡張するように構成できます。</span><span class="sxs-lookup"><span data-stu-id="f6713-104">The following globalization services can be configured to extend the capabilities that exist in some Microsoft Dynamics 365 online services:</span></span>

- <span data-ttu-id="f6713-105">**Regulatory Configuration Service (RCS)** は、さまざまなタイプの電子ドキュメントおよびレポート の構成をサポートします。</span><span class="sxs-lookup"><span data-stu-id="f6713-105">**Regulatory Configuration Service (RCS)** supports the configuration of different types of electronic documents and reports.</span></span> <span data-ttu-id="f6713-106">RCS はコンフィギュレーション リポジトリがスタンドアロンのサービスである、電子申告 (ER) の デザイナーの拡張バージョンを提供します。</span><span class="sxs-lookup"><span data-stu-id="f6713-106">RCS provides an enhanced version of the Electronic reporting (ER) designer where the configuration repository is a standalone service.</span></span> <span data-ttu-id="f6713-107">詳細については、[Regulatory Configuration Service](rcs-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f6713-107">For more information, see [Regulatory Configuration Service](rcs-overview.md).</span></span>
- <span data-ttu-id="f6713-108">**電子請求** は、変換、デジタル署名、および認証や応答処理などの外部 Web サービスとの接続のための構成可能な統合のための構成可能な形式をまとめたものです。</span><span class="sxs-lookup"><span data-stu-id="f6713-108">**Electronic Invoicing** brings together configurable formats for transformations, digital signatures, and configurable integrations for connectivity with external web services, including certification and response handling.</span></span> <span data-ttu-id="f6713-109">詳細については、[電子請求](e-invoicing-service-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f6713-109">For more information, see [Electronic Invoicing](e-invoicing-service-overview.md).</span></span>
- <span data-ttu-id="f6713-110">**税計算** は、複数の税 ID、税コード決定、税計算デザイナー、および世界中の複雑な税規制に準拠するランタイム エンジンをサポートすることにより、柔軟性を強化します。</span><span class="sxs-lookup"><span data-stu-id="f6713-110">**Tax Calculation** provides enhanced flexibility by supporting multiple tax IDs, tax code determination, the tax calculation designer, and a runtime engine to comply with complex tax regulations worldwide.</span></span> <span data-ttu-id="f6713-111">詳細については、[税の計算](global-tax-calcuation-service-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f6713-111">For more information, see [Tax Calculation](global-tax-calcuation-service-overview.md).</span></span>

<span data-ttu-id="f6713-112">これらのグローバリゼーション サービスは、次の Dynamics 365 オンライン サービスと一新された統合を提供します。</span><span class="sxs-lookup"><span data-stu-id="f6713-112">These globalization services provide out-of-box integration with the following Dynamics 365 online services.</span></span>

| <span data-ttu-id="f6713-113">オンライン サービス</span><span class="sxs-lookup"><span data-stu-id="f6713-113">Online service</span></span> | <span data-ttu-id="f6713-114">RCS</span><span class="sxs-lookup"><span data-stu-id="f6713-114">RCS</span></span> | <span data-ttu-id="f6713-115">電子請求</span><span class="sxs-lookup"><span data-stu-id="f6713-115">Electronic Invoicing</span></span> | <span data-ttu-id="f6713-116">税の計算 (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="f6713-116">Tax Calculation (Preview)</span></span> |
|----------------|-----|----------------------|---------------------------|
| <span data-ttu-id="f6713-117">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="f6713-117">Dynamics 365 Finance</span></span> | <span data-ttu-id="f6713-118">あり</span><span class="sxs-lookup"><span data-stu-id="f6713-118">Yes</span></span> | <span data-ttu-id="f6713-119">あり</span><span class="sxs-lookup"><span data-stu-id="f6713-119">Yes</span></span> | <span data-ttu-id="f6713-120">あり</span><span class="sxs-lookup"><span data-stu-id="f6713-120">Yes</span></span> | 
| <span data-ttu-id="f6713-121">Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="f6713-121">Dynamics 365 Supply Chain Management</span></span> | <span data-ttu-id="f6713-122">あり</span><span class="sxs-lookup"><span data-stu-id="f6713-122">Yes</span></span> | <span data-ttu-id="f6713-123">あり</span><span class="sxs-lookup"><span data-stu-id="f6713-123">Yes</span></span> | <span data-ttu-id="f6713-124">あり</span><span class="sxs-lookup"><span data-stu-id="f6713-124">Yes</span></span> | 
| <span data-ttu-id="f6713-125">Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="f6713-125">Dynamics 365 Project Operations</span></span> | <span data-ttu-id="f6713-126">あり</span><span class="sxs-lookup"><span data-stu-id="f6713-126">Yes</span></span> | <span data-ttu-id="f6713-127">あり</span><span class="sxs-lookup"><span data-stu-id="f6713-127">Yes</span></span> | <span data-ttu-id="f6713-128">適用できません</span><span class="sxs-lookup"><span data-stu-id="f6713-128">Not applicable</span></span> | 
| <span data-ttu-id="f6713-129">Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f6713-129">Dynamics 365 Commerce</span></span> | <span data-ttu-id="f6713-130">あり</span><span class="sxs-lookup"><span data-stu-id="f6713-130">Yes</span></span> | <span data-ttu-id="f6713-131">適用できません</span><span class="sxs-lookup"><span data-stu-id="f6713-131">Not applicable</span></span> | <span data-ttu-id="f6713-132">適用できません</span><span class="sxs-lookup"><span data-stu-id="f6713-132">Not applicable</span></span> | 

> [!NOTE]
> <span data-ttu-id="f6713-133">RCS の Azure 地理的場所 (地理) の可用性が異なるため、このサービスの構成により、該当する Dynamics 365 オンライン サービスに選択された地理的な場所の外部に顧客データが転送される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f6713-133">Because of differences in the availability of Azure geographic locations (geos) for RCS, configuration of this service might cause customer data to be transferred outside the geo that is selected for the applicable Dynamics 365 online service.</span></span> <span data-ttu-id="f6713-134">詳細については [Dynamics 365 および Power Platform: 使用可能性、データの場所、言語、およびローカライズを参照してください](https://aka.ms/rcs/D365Productavailabilityguide)。</span><span class="sxs-lookup"><span data-stu-id="f6713-134">For more information, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/rcs/D365Productavailabilityguide).</span></span>