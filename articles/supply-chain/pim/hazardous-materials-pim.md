---
title: 危険物
description: このトピックでは、環境に保存されている危険物ドキュメントおよび情報に関する情報を提供します。
author: lachlancashMS
manager: tfehr
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 079c8d23250368c92e5d79f0e2624f8340db2077
ms.sourcegitcommit: c009ec75f53872272f11c92a1ce81a391e3845a2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/18/2020
ms.locfileid: "3699539"
---
# <a name="hazardous-materials"></a><span data-ttu-id="837ed-103">危険物</span><span class="sxs-lookup"><span data-stu-id="837ed-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="837ed-104">危険物に関する情報は、製品情報管理で設定されています。</span><span class="sxs-lookup"><span data-stu-id="837ed-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="837ed-105">このモジュールでは、倉庫管理を使用して印刷できるドキュメントも提供します。</span><span class="sxs-lookup"><span data-stu-id="837ed-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="837ed-106">危険物として分類される材料を出荷する場合は、その出荷に対して追加の書類を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="837ed-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="837ed-107">危険物の機能により、顧客は分類情報を保存し、それをリリース品目に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="837ed-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="837ed-108">この情報は、船積書類を準備するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="837ed-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="837ed-109">Microsoft Dynamics 365 Supply Chain Management の危険物機能には、危険な製品に関連する情報の記録と参照に役立つ、有用な製品情報フィールドと関連機能のコレクションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="837ed-109">The hazardous materials features in Microsoft Dynamics 365 Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="837ed-110">これらの機能は、出荷する危険物に関する同じ情報を含む出荷ドキュメントの設計と印刷にも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="837ed-110">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="837ed-111">ただし、システムがお客様の国または地域で適用されるすべての規制に自動的に準拠することはありません。</span><span class="sxs-lookup"><span data-stu-id="837ed-111">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="837ed-112">これらのツールは、一般的な規制への準拠を支援することを目的としていますが、それだけでは十分ではなく、そうであることを保証するものでもありません。</span><span class="sxs-lookup"><span data-stu-id="837ed-112">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="837ed-113">組織は、適用されるすべての規制を把握し、それらを遵守するために必要なすべての措置を講じる責任があります。</span><span class="sxs-lookup"><span data-stu-id="837ed-113">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

<span data-ttu-id="837ed-114">この機能を使用する前に、次の設定が必要です。</span><span class="sxs-lookup"><span data-stu-id="837ed-114">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="837ed-115">**製品情報管理:** リリース済製品に適用できるコードを設定します。</span><span class="sxs-lookup"><span data-stu-id="837ed-115">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="837ed-116">**倉庫管理:** 出荷情報を印刷するには、追加の出荷ドキュメントを使用します。</span><span class="sxs-lookup"><span data-stu-id="837ed-116">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="837ed-117">製品情報管理</span><span class="sxs-lookup"><span data-stu-id="837ed-117">Product information management</span></span>

<span data-ttu-id="837ed-118">製品情報管理には、陸路、航空、および海上貨物の危険物リストで提供される参照情報を追加できる一連の設定テーブルがあります。</span><span class="sxs-lookup"><span data-stu-id="837ed-118">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="837ed-119">よく参照される規制の一部を次に示します。</span><span class="sxs-lookup"><span data-stu-id="837ed-119">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="837ed-120">**ADR** – 陸路による危険物の国際輸送に関連する規制</span><span class="sxs-lookup"><span data-stu-id="837ed-120">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="837ed-121">**CFR 49** – 危険物の輸送に関する米国の規制</span><span class="sxs-lookup"><span data-stu-id="837ed-121">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="837ed-122">**IMDG** – 国際海上危険物規則 (IMDG) コード</span><span class="sxs-lookup"><span data-stu-id="837ed-122">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="837ed-123">**IATA** – 国際航空運送協会 (IATA) 危険物規制</span><span class="sxs-lookup"><span data-stu-id="837ed-123">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="837ed-124">これらの各規制には、参照コードを含む危険物の一覧があります。</span><span class="sxs-lookup"><span data-stu-id="837ed-124">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="837ed-125">輸送の各タイプのリストは、共有国際分類で結合されます。</span><span class="sxs-lookup"><span data-stu-id="837ed-125">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="837ed-126">Supply Chain Management には、これらのリストの共有コードの参照テーブルが用意されています。</span><span class="sxs-lookup"><span data-stu-id="837ed-126">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="837ed-127">また、各リストには、定義可能な一意のコードもいくつか含まれています。</span><span class="sxs-lookup"><span data-stu-id="837ed-127">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="837ed-128">この情報の構成を開始するには、初期パラメーターを構成するために使用できる規制を作成します。</span><span class="sxs-lookup"><span data-stu-id="837ed-128">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="837ed-129">倉庫管理</span><span class="sxs-lookup"><span data-stu-id="837ed-129">Warehouse management</span></span>

<span data-ttu-id="837ed-130">出荷の準備ができると、いくつかの新しいレポートを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="837ed-130">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="837ed-131">これらのレポートでは、製品情報管理で設定した情報が使用されます。</span><span class="sxs-lookup"><span data-stu-id="837ed-131">These reports use the information that you set up in Product information management.</span></span>
