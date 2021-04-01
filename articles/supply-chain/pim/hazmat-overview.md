---
title: 危険物の概要
description: このトピックでは、製品情報管理と倉庫管理の際における危険物の処理および文書化に関連する機能の概要を示します。
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 4ff997214f80d97f6e558d32fbf66663cbc84143
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231891"
---
# <a name="hazardous-materials-overview"></a><span data-ttu-id="e311d-103">危険物の概要</span><span class="sxs-lookup"><span data-stu-id="e311d-103">Hazardous materials overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="e311d-104">送料と配送の規制を維持するには、危険商品として分類された材料を出荷する組織には、その出荷を伴う追加の書類を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="e311d-104">To remain compliant with shipping and transport regulations, organizations that ship materials that are classified as dangerous goods must include additional paperwork with their shipments.</span></span> <span data-ttu-id="e311d-105">危険物機能により、顧客はリリースされた品目に関する情報を保存することができます。</span><span class="sxs-lookup"><span data-stu-id="e311d-105">The hazardous materials feature lets customers store information that is related to released items.</span></span> <span data-ttu-id="e311d-106">この情報は、船積書類を準備するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="e311d-106">This information can then be used to help prepare shipping documentation.</span></span> <span data-ttu-id="e311d-107">危険な商品を出荷する組織には、出荷プロセスを管理するための独自のプロセスと手順が必要です。</span><span class="sxs-lookup"><span data-stu-id="e311d-107">An organization that ships dangerous goods must have its own processes and procedures for managing the shipping process.</span></span> <span data-ttu-id="e311d-108">Microsoft Dynamics 365 Supply Chain Managementは、必要なドキュメントの生成を支援するためのツールでしかありません。</span><span class="sxs-lookup"><span data-stu-id="e311d-108">Microsoft Dynamics 365 Supply Chain Management is just a tool that can help generate the required documents.</span></span>

<span data-ttu-id="e311d-109">次の図は、危険物機能を設定および使用するために必要な手順を示しています。</span><span class="sxs-lookup"><span data-stu-id="e311d-109">The following diagram illustrates the steps needed to set up and use the hazardous materials feature.</span></span>

<span data-ttu-id="e311d-110">![危険物機能の設定および使用](media/hazmat-overview.png "危険物機能の設定および使用")</span><span class="sxs-lookup"><span data-stu-id="e311d-110">![Setup and use of the hazardous materials feature](media/hazmat-overview.png "Setup and use of the hazardous materials feature")</span></span>

<span data-ttu-id="e311d-111">危険物の機能は、製品情報管理で設定されており、倉庫管理を使用して印刷できるドキュメントが用意されています。</span><span class="sxs-lookup"><span data-stu-id="e311d-111">The hazardous materials feature is set up in Product information management and provides documents that can be printed through Warehouse management.</span></span> <span data-ttu-id="e311d-112">したがって、このような領域は、次の 2 つの主要領域で、この機能の確認、設定、および使用を行います。</span><span class="sxs-lookup"><span data-stu-id="e311d-112">Therefore, broadly speaking, those areas are the two main areas where you will review, set up, and use this feature's functionality:</span></span>

- <span data-ttu-id="e311d-113">**製品情報管理** - リリース済製品に適用できるコードを設定します。</span><span class="sxs-lookup"><span data-stu-id="e311d-113">**Product information management** – Set up the codes that will be applied to a released product.</span></span>
- <span data-ttu-id="e311d-114">**倉庫管理** - 出荷用に印刷される追加の出荷ドキュメントと機能します。</span><span class="sxs-lookup"><span data-stu-id="e311d-114">**Warehouse management** – Work with additional shipping documents that will be printed for shipments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e311d-115">Supply Chain Management の危険物機能には、危険な製品に関連する情報の記録と参照に役立つ、有用な製品情報フィールドと関連機能のコレクションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="e311d-115">The hazardous materials features in Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="e311d-116">これらの機能は、出荷する危険物に関する同じ情報を含む出荷ドキュメントの設計と印刷にも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="e311d-116">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="e311d-117">ただし、システムがお客様の国または地域で適用されるすべての規制に自動的に準拠することはありません。</span><span class="sxs-lookup"><span data-stu-id="e311d-117">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="e311d-118">これらのツールは、一般的な規制への準拠を支援することを目的としていますが、それだけでは十分ではなく、そうであることを保証するものでもありません。</span><span class="sxs-lookup"><span data-stu-id="e311d-118">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="e311d-119">組織は、適用されるすべての規制を把握し、それらを遵守するために必要なすべての措置を講じる責任があります。</span><span class="sxs-lookup"><span data-stu-id="e311d-119">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="e311d-120">製品情報管理</span><span class="sxs-lookup"><span data-stu-id="e311d-120">Product information management</span></span>

<span data-ttu-id="e311d-121">製品情報管理には、陸路、航空、および海上貨物の様々な危険物リストで提供される参照情報を入力できる一連の設定テーブルがあります。</span><span class="sxs-lookup"><span data-stu-id="e311d-121">Product information management provides a range of setup tables where you can enter reference information for the various dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="e311d-122">この機能が開発された場合、次のような一般的な規制が参照されています。</span><span class="sxs-lookup"><span data-stu-id="e311d-122">The following common regulations were referenced when this functionality was developed:</span></span>

- <span data-ttu-id="e311d-123">**ADR** – 陸路による危険物の国際輸送に関連する規制</span><span class="sxs-lookup"><span data-stu-id="e311d-123">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="e311d-124">**CFR 49** – 危険物の輸送に関する米国の規制</span><span class="sxs-lookup"><span data-stu-id="e311d-124">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="e311d-125">**IMDG** – 国際海上危険物規則 (IMDG) コード</span><span class="sxs-lookup"><span data-stu-id="e311d-125">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="e311d-126">**IATA** – 国際航空運送協会 (IATA) 危険物規制</span><span class="sxs-lookup"><span data-stu-id="e311d-126">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="e311d-127">各規制には、危険な商品および参照コードが標準化されています。</span><span class="sxs-lookup"><span data-stu-id="e311d-127">Each set of regulations provides standardized lists of dangerous goods and reference codes.</span></span> <span data-ttu-id="e311d-128">従って、Supply Chain Management には、これらのリストの共有コードの参照テーブルが用意されています。</span><span class="sxs-lookup"><span data-stu-id="e311d-128">Therefore, Supply Chain Management provides a reference table for the common codes on those lists.</span></span> <span data-ttu-id="e311d-129">また、各リストには、定義可能な一意のコードもいくつか含まれています。</span><span class="sxs-lookup"><span data-stu-id="e311d-129">Each list also has some unique codes that you can define.</span></span>

<span data-ttu-id="e311d-130">危険物の規則や値を設定する方法と、その値を適切な製品に割り当てる方法の詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e311d-130">For more information about how to set up regulations and values for hazardous materials, and how to assign the values to relevant products, see the following topics:</span></span>

- [<span data-ttu-id="e311d-131">危険物の設定</span><span class="sxs-lookup"><span data-stu-id="e311d-131">Set up hazardous materials</span></span>](hazmat-setup.md)
- [<span data-ttu-id="e311d-132">製品、注文、出荷、積荷の危険物</span><span class="sxs-lookup"><span data-stu-id="e311d-132">Hazardous materials in products, orders, shipments, and loads</span></span>](hazmat-items.md)

## <a name="warehouse-management"></a><span data-ttu-id="e311d-133">倉庫管理</span><span class="sxs-lookup"><span data-stu-id="e311d-133">Warehouse management</span></span>

<span data-ttu-id="e311d-134">倉庫管理で出荷を準備すると、製品情報管理で設定した情報を使用するいくつかの新しいレポートを印刷できるようになります。</span><span class="sxs-lookup"><span data-stu-id="e311d-134">When you prepare a shipment in Warehouse management, you will be able to print several new reports that use the information that you set up in Product information management.</span></span> <span data-ttu-id="e311d-135">利用可能なレポートとその使用方法の詳細については、[危険物の照会およびレポート](hazmat-reports.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e311d-135">For more information about the available reports and how to use them, see [Hazardous materials inquiries and reports](hazmat-reports.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]