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
ms.openlocfilehash: 5006f06d90ddcc314a51878e9e21337de7d493e7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208468"
---
# <a name="hazardous-materials"></a><span data-ttu-id="b57f2-103">危険物</span><span class="sxs-lookup"><span data-stu-id="b57f2-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b57f2-104">危険物に関する情報は、製品情報管理で設定されています。</span><span class="sxs-lookup"><span data-stu-id="b57f2-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="b57f2-105">このモジュールでは、倉庫管理を使用して印刷できるドキュメントも提供します。</span><span class="sxs-lookup"><span data-stu-id="b57f2-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="b57f2-106">危険物として分類される材料を出荷する場合は、その出荷に対して追加の書類を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="b57f2-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="b57f2-107">危険物の機能により、顧客は分類情報を保存し、それをリリース品目に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="b57f2-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="b57f2-108">この情報は、船積書類を準備するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="b57f2-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b57f2-109">Microsoft Dynamics 365 Supply Chain Management では、危険物の出荷を管理するために、製品に関連する追加の参照情報を設定できます。</span><span class="sxs-lookup"><span data-stu-id="b57f2-109">To help manage shipments of dangerous goods, Microsoft Dynamics 365 Supply Chain Management lets you set up additional reference information that is related to products.</span></span> <span data-ttu-id="b57f2-110">追加の出荷ドキュメントを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="b57f2-110">You can also set up additional shipment documents.</span></span> <span data-ttu-id="b57f2-111">ただし、システムはお客様の国または地域の規制に自動的に準拠しているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="b57f2-111">However, the system isn't automatically compliant with your country's or region's regulations.</span></span> <span data-ttu-id="b57f2-112">その代わりに、プログラム全体を支援するツールです。</span><span class="sxs-lookup"><span data-stu-id="b57f2-112">Instead, it's a tool that can help your overall program.</span></span>

<span data-ttu-id="b57f2-113">この機能を使用する前に、次の設定が必要です。</span><span class="sxs-lookup"><span data-stu-id="b57f2-113">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="b57f2-114">**製品情報管理:** リリース済製品に適用できるコードを設定します。</span><span class="sxs-lookup"><span data-stu-id="b57f2-114">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="b57f2-115">**倉庫管理:** 出荷情報を印刷するには、追加の出荷ドキュメントを使用します。</span><span class="sxs-lookup"><span data-stu-id="b57f2-115">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="b57f2-116">製品情報管理</span><span class="sxs-lookup"><span data-stu-id="b57f2-116">Product information management</span></span>

<span data-ttu-id="b57f2-117">製品情報管理には、陸路、航空、および海上貨物の危険物リストで提供される参照情報を追加できる一連の設定テーブルがあります。</span><span class="sxs-lookup"><span data-stu-id="b57f2-117">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="b57f2-118">よく参照される規制の一部を次に示します。</span><span class="sxs-lookup"><span data-stu-id="b57f2-118">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="b57f2-119">**ADR** – 陸路による危険物の国際輸送に関連する規制</span><span class="sxs-lookup"><span data-stu-id="b57f2-119">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="b57f2-120">**CFR 49** – 危険物の輸送に関する米国の規制</span><span class="sxs-lookup"><span data-stu-id="b57f2-120">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="b57f2-121">**IMDG** – 国際海上危険物規則 (IMDG) コード</span><span class="sxs-lookup"><span data-stu-id="b57f2-121">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="b57f2-122">**IATA** – 国際航空運送協会 (IATA) 危険物規制</span><span class="sxs-lookup"><span data-stu-id="b57f2-122">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="b57f2-123">これらの各規制には、参照コードを含む危険物の一覧があります。</span><span class="sxs-lookup"><span data-stu-id="b57f2-123">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="b57f2-124">輸送の各タイプのリストは、共有国際分類で結合されます。</span><span class="sxs-lookup"><span data-stu-id="b57f2-124">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="b57f2-125">Supply Chain Management には、これらのリストの共有コードの参照テーブルが用意されています。</span><span class="sxs-lookup"><span data-stu-id="b57f2-125">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="b57f2-126">また、各リストには、定義可能な一意のコードもいくつか含まれています。</span><span class="sxs-lookup"><span data-stu-id="b57f2-126">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="b57f2-127">この情報の構成を開始するには、初期パラメーターを構成するために使用できる規制を作成します。</span><span class="sxs-lookup"><span data-stu-id="b57f2-127">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="b57f2-128">倉庫管理</span><span class="sxs-lookup"><span data-stu-id="b57f2-128">Warehouse management</span></span>

<span data-ttu-id="b57f2-129">出荷の準備ができると、いくつかの新しいレポートを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="b57f2-129">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="b57f2-130">これらのレポートでは、製品情報管理で設定した情報が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b57f2-130">These reports use the information that you set up in Product information management.</span></span>
