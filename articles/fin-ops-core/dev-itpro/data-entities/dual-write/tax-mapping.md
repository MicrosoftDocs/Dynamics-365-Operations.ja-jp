---
title: 統合された税
description: このトピックでは、Finance and Operations と Common Data Service 間の税データの統合について説明します。
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
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
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: a4da37d45698290b40f6c72148f1500bef72127a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173088"
---
# <a name="integrated-tax"></a><span data-ttu-id="77ed6-103">統合された税</span><span class="sxs-lookup"><span data-stu-id="77ed6-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="77ed6-104">税設定データでは、間接税 (VAT、GST、売上税) および源泉徴収税の両方の設定が定義されます。</span><span class="sxs-lookup"><span data-stu-id="77ed6-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="77ed6-105">税金計算ルール、税率、税務会計、決済、およびその他の概念について説明します。</span><span class="sxs-lookup"><span data-stu-id="77ed6-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="77ed6-106">テンプレート</span><span class="sxs-lookup"><span data-stu-id="77ed6-106">Templates</span></span>

<span data-ttu-id="77ed6-107">次の表に示すように、税データには、データ操作中に連携して動作するエンティティ マップのコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="77ed6-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="77ed6-108">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="77ed6-108">Finance and Operations apps</span></span> | <span data-ttu-id="77ed6-109">Dynamics 365 のモデル駆動型アプリ</span><span class="sxs-lookup"><span data-stu-id="77ed6-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="77ed6-110">説明</span><span class="sxs-lookup"><span data-stu-id="77ed6-110">Description</span></span> |
-------------------------|---------------------------------
<span data-ttu-id="77ed6-111">税コード</span><span class="sxs-lookup"><span data-stu-id="77ed6-111">Tax codes</span></span>                   | <span data-ttu-id="77ed6-112">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="77ed6-112">msdyn\_taxcodes.md</span></span> | 
<span data-ttu-id="77ed6-113">税グループ</span><span class="sxs-lookup"><span data-stu-id="77ed6-113">Tax groups</span></span>                 | <span data-ttu-id="77ed6-114">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="77ed6-114">msdyn\_taxgroups.md</span></span> | 
<span data-ttu-id="77ed6-115">税品目グループ</span><span class="sxs-lookup"><span data-stu-id="77ed6-115">Tax item groups</span></span>             | <span data-ttu-id="77ed6-116">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="77ed6-116">msdyn\_taxitemgroups.md</span></span> | 
<span data-ttu-id="77ed6-117">免税</span><span class="sxs-lookup"><span data-stu-id="77ed6-117">Tax Exemptions</span></span>             | <span data-ttu-id="77ed6-118">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="77ed6-118">msdyn\_taxexemptcodes.md</span></span> | 
<span data-ttu-id="77ed6-119">税務当局</span><span class="sxs-lookup"><span data-stu-id="77ed6-119">Tax Authorities</span></span>             | <span data-ttu-id="77ed6-120">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="77ed6-120">msdyn\_taxauthorities.md</span></span> | 
<span data-ttu-id="77ed6-121">源泉徴収税コード</span><span class="sxs-lookup"><span data-stu-id="77ed6-121">Withholding tax codes</span></span>       | <span data-ttu-id="77ed6-122">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="77ed6-122">msdyn\_withholdingtaxcodes.md</span></span> | 
<span data-ttu-id="77ed6-123">源泉徴収税グループ</span><span class="sxs-lookup"><span data-stu-id="77ed6-123">Withholding tax groups</span></span>     | <span data-ttu-id="77ed6-124">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="77ed6-124">msdyn\_withholdingtaxgroups.md</span></span> | 
<span data-ttu-id="77ed6-125">税勘定科目グループ</span><span class="sxs-lookup"><span data-stu-id="77ed6-125">Tax Ledger Account Group</span></span> | <span data-ttu-id="77ed6-126">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="77ed6-126">msdyn\_taxpostinggroups</span></span>     | 

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

