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
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 68461f375c6d5b04f224331dc192c921cf3c4d04
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979332"
---
# <a name="integrated-tax"></a><span data-ttu-id="67d4a-103">統合された税</span><span class="sxs-lookup"><span data-stu-id="67d4a-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="67d4a-104">税設定データでは、間接税 (VAT、GST、売上税) および源泉徴収税の両方の設定が定義されます。</span><span class="sxs-lookup"><span data-stu-id="67d4a-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="67d4a-105">税金計算ルール、税率、税務会計、決済、およびその他の概念について説明します。</span><span class="sxs-lookup"><span data-stu-id="67d4a-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="67d4a-106">テンプレート</span><span class="sxs-lookup"><span data-stu-id="67d4a-106">Templates</span></span>

<span data-ttu-id="67d4a-107">次の表に示すように、税データには、データ操作中に連携して動作するエンティティ マップのコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="67d4a-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="67d4a-108">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="67d4a-108">Finance and Operations apps</span></span> | <span data-ttu-id="67d4a-109">Dynamics 365 のモデル駆動型アプリ</span><span class="sxs-lookup"><span data-stu-id="67d4a-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="67d4a-110">説明</span><span class="sxs-lookup"><span data-stu-id="67d4a-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="67d4a-111">品目売上税グループ</span><span class="sxs-lookup"><span data-stu-id="67d4a-111">Item sales tax group</span></span> | <span data-ttu-id="67d4a-112">msdyn_taxitemgroups</span><span class="sxs-lookup"><span data-stu-id="67d4a-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="67d4a-113">消費税所轄官庁</span><span class="sxs-lookup"><span data-stu-id="67d4a-113">Sales tax authorities</span></span> | <span data-ttu-id="67d4a-114">msdyn_taxauthorities</span><span class="sxs-lookup"><span data-stu-id="67d4a-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="67d4a-115">消費税非課税コード エンティティ CDS</span><span class="sxs-lookup"><span data-stu-id="67d4a-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="67d4a-116">msdyn_taxexemptcodes</span><span class="sxs-lookup"><span data-stu-id="67d4a-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="67d4a-117">消費税グループ</span><span class="sxs-lookup"><span data-stu-id="67d4a-117">Sales tax groups</span></span> | <span data-ttu-id="67d4a-118">msdyn_taxgroups</span><span class="sxs-lookup"><span data-stu-id="67d4a-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="67d4a-119">消費税元帳転記グループ V2</span><span class="sxs-lookup"><span data-stu-id="67d4a-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="67d4a-120">msdyn_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="67d4a-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="67d4a-121">源泉徴収税コード</span><span class="sxs-lookup"><span data-stu-id="67d4a-121">Withholding tax codes</span></span> | <span data-ttu-id="67d4a-122">msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="67d4a-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="67d4a-123">源泉徴収税グループ</span><span class="sxs-lookup"><span data-stu-id="67d4a-123">Withholding tax groups</span></span> | <span data-ttu-id="67d4a-124">msdyn_withholdingtaxgroups</span><span class="sxs-lookup"><span data-stu-id="67d4a-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

