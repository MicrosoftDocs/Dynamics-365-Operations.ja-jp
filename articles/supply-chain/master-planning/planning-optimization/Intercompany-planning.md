---
title: 会社間計画
description: このトピックでは、会社間計画について説明し、Microsoft Dynamics 365 Supply Chain Management で計画の最適化を使用して会社間計画を構成する方法を説明します。
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 25c80ce27498131c6eb92174ab14a592bfa9915a
ms.sourcegitcommit: fe21a3a98dcf6fe4eb9351941493f2c0443d8696
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672194"
---
# <a name="intercompany-planning"></a><span data-ttu-id="7df5e-103">会社間計画</span><span class="sxs-lookup"><span data-stu-id="7df5e-103">Intercompany planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7df5e-104">組織によっては、物流工程が組織内の他の法人 (会社) に依存している場合もあります。</span><span class="sxs-lookup"><span data-stu-id="7df5e-104">For some organizations, logistics operations depend on other legal entities (companies) in the organization.</span></span> <span data-ttu-id="7df5e-105">各法人が個別の勘定科目表を所有するため、これらの工程は会社間の販売と購買を使用して処理されます。</span><span class="sxs-lookup"><span data-stu-id="7df5e-105">These operations are handled by using intercompany sales and purchases, because each legal entity has a separate chart of accounts.</span></span>

<span data-ttu-id="7df5e-106">このトピックでは、会社間計画について説明し、Microsoft Dynamics 365 Supply Chain Management で計画の最適化を使用して会社間計画を構成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="7df5e-106">This topic describes intercompany planning and explains how to configure intercompany planning with Planning Optimization in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="7df5e-107">このトピックでは、次の重要な会社間用語を使用します。</span><span class="sxs-lookup"><span data-stu-id="7df5e-107">This topic uses the following important intercompany terms:</span></span>

- <span data-ttu-id="7df5e-108">**上流** – 会社またはサプライ チェーンの相対的な参照。</span><span class="sxs-lookup"><span data-stu-id="7df5e-108">**Upstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="7df5e-109">原材料サプライヤーの方向から流れるデータの動きを示します。</span><span class="sxs-lookup"><span data-stu-id="7df5e-109">It indicates movement in the direction of the raw material supplier.</span></span>
- <span data-ttu-id="7df5e-110">**下流** – 会社またはサプライ チェーンの相対的な参照。</span><span class="sxs-lookup"><span data-stu-id="7df5e-110">**Downstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="7df5e-111">顧客の方向から流れるデータの動きを示します。</span><span class="sxs-lookup"><span data-stu-id="7df5e-111">It indicates movement in the direction of the customer.</span></span>
- <span data-ttu-id="7df5e-112">**計画企業内需要** – 下流会社からの製品の計画需要に基づいた、会社の製品に対する計画需要。</span><span class="sxs-lookup"><span data-stu-id="7df5e-112">**Planned intercompany demand** – Planned demand for a product in a company, based on planned demand for the product from a downstream company.</span></span>

<span data-ttu-id="7df5e-113">マスター プランでは、会社の計画には、別の会社の計画からの計画オーダーに関連する計画企業内需要を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7df5e-113">In master planning, a plan in one company can include planned intercompany demand that is related to planned orders from a plan in another company.</span></span> <span data-ttu-id="7df5e-114">この機能を使用すると、複数の会社間で計画オーダーの完全な透明性が実現するので便利です。</span><span class="sxs-lookup"><span data-stu-id="7df5e-114">This capability is useful, because it provides full visibility into planned orders across companies.</span></span> <span data-ttu-id="7df5e-115">また、必要なすべての計画供給オーダーが作成されますが、会社間需要に対して計画オーダーを確定する必要がありません。</span><span class="sxs-lookup"><span data-stu-id="7df5e-115">It also ensures that all required planned supply orders are created, but without requiring that planned orders be firmed for the intercompany demand.</span></span>

<span data-ttu-id="7df5e-116">計画されたダウンストリームの需要を含むマスター プランからマスター プランを実行する場合は、関連する会社間仕入先からの計画発注書が需要として計画に含まれます。</span><span class="sxs-lookup"><span data-stu-id="7df5e-116">If you run master planning from a master plan that includes planned downstream demand, planned purchase orders from the related intercompany vendors will be included in the plan as demand.</span></span>

## <a name="required-setup"></a><span data-ttu-id="7df5e-117">必要な設定</span><span class="sxs-lookup"><span data-stu-id="7df5e-117">Required setup</span></span>

<span data-ttu-id="7df5e-118">会社間計画を使用するには、次のようにシステムを準備する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7df5e-118">To use intercompany planning, you must prepare your system in the following way:</span></span>

1. <span data-ttu-id="7df5e-119">関連する製品は、関連するすべての会社でリリースする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7df5e-119">The relevant products must be released in all the relevant companies.</span></span> <span data-ttu-id="7df5e-120">詳細については、Microsoft Learn で [Dynamics 365 Supply Chain Management で会社間取引を構成および使用する](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7df5e-120">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="7df5e-121">上流会社や関連する既定の在庫分析コード (サイトと倉庫) との会社間リレーションがある仕入先の購買で、ダウンストリームの需要をカバーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7df5e-121">Downstream demand must be covered by purchases from a vendor that has an intercompany relation to the upstream company and relevant default inventory dimensions (site and warehouse) on the customer.</span></span> <span data-ttu-id="7df5e-122">詳細については、Microsoft Learn で [Dynamics 365 Supply Chain Management で会社間取引を構成および使用する](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7df5e-122">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="7df5e-123">上流会社のマスター プランには、計画された下流需要を含める必要があります。また、関連する会社とマスター プランを下流計画で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7df5e-123">The master plan in the upstream company must include planned downstream demand, and the relevant company and master plan must be specified in the downstream plans.</span></span>

## <a name="include-planned-downstream-demand"></a><span data-ttu-id="7df5e-124">下流の計画需要を含める</span><span class="sxs-lookup"><span data-stu-id="7df5e-124">Include planned downstream demand</span></span>

<span data-ttu-id="7df5e-125">計画された下流需要が計画に含まれるようにマスター プランを構成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7df5e-125">Follow these steps to configure your master plan so that it includes planned downstream demand.</span></span>

1. <span data-ttu-id="7df5e-126">**マスター プラン \> 設定 \> プラン \> マスター プラン** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7df5e-126">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="7df5e-127">マスター プランを選択または作成します。</span><span class="sxs-lookup"><span data-stu-id="7df5e-127">Select or create a master plan.</span></span>
1. <span data-ttu-id="7df5e-128">**会社間計画** クイック タブで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="7df5e-128">On the **Intercompany planning** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="7df5e-129">**計画された下流需要を含める** – このオプションを *はい* に設定して、マスター プランの会社間計画を有効にします。</span><span class="sxs-lookup"><span data-stu-id="7df5e-129">**Include planned downstream demand** – Set this option to *Yes* to enable intercompany planning for the master plan.</span></span>
    - <span data-ttu-id="7df5e-130">**下流計画** – **計画された下流需要を含める** オプションを *はい* に設定すると、ツール バーとグリッドを使用して、他の会社から要求されたマスター プランを追加できます。</span><span class="sxs-lookup"><span data-stu-id="7df5e-130">**Downstream plans** – If you set the **Include planned downstream demand** option to *Yes*, use the toolbar and grid to add the desired master plans from other companies.</span></span>

## <a name="peg-across-companies-by-using-multilevel-pegging"></a><span data-ttu-id="7df5e-131">複数レベルのペギングを使用して、複数の会社をペギングする</span><span class="sxs-lookup"><span data-stu-id="7df5e-131">Peg across companies by using multilevel pegging</span></span>

<span data-ttu-id="7df5e-132">複数レベルのペギングでは、会社間のペギングを表示してサプライがカバーした需要元を確認できます。</span><span class="sxs-lookup"><span data-stu-id="7df5e-132">In multilevel pegging, you can view pegging across companies to see the initial source of demand that is being covered by a supply.</span></span>

<span data-ttu-id="7df5e-133">複数レベルのペギング情報を表示するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="7df5e-133">To view multilevel pegging information, follow these steps.</span></span>

1. <span data-ttu-id="7df5e-134">**マスター プラン \> マスタープラン \> 計画オーダー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7df5e-134">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="7df5e-135">計画オーダーを、選択するか、表示します。</span><span class="sxs-lookup"><span data-stu-id="7df5e-135">Select or open a planned order.</span></span>
1. <span data-ttu-id="7df5e-136">アクション ペインの **表示** タブ、**要件** グループで、**複数レベルのぺギング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7df5e-136">On the Action Pane, on the **View** tab, in the **Requirements** group, select **Multilevel pegging**.</span></span>

### <a name="intercompany-example-that-involves-two-companies"></a><span data-ttu-id="7df5e-137">2 つの会社が関わる会社間の例</span><span class="sxs-lookup"><span data-stu-id="7df5e-137">Intercompany example that involves two companies</span></span>

<span data-ttu-id="7df5e-138">この例では、USMF 会社で計画製造オーダーを作成し、DEMF 会社で販売注文をカバーします。</span><span class="sxs-lookup"><span data-stu-id="7df5e-138">For this example, a planned production order is created in the USMF company to cover a sales order in the DEMF company.</span></span> <span data-ttu-id="7df5e-139">USMF では、直接需要は計画企業内需要です。</span><span class="sxs-lookup"><span data-stu-id="7df5e-139">In USMF, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="7df5e-140">この需要を USMF で表示するには、マスター プランをまず DEMF で実行してから USMF で実行します。</span><span class="sxs-lookup"><span data-stu-id="7df5e-140">To make this demand appear in USMF, master planning is run first in DEMF and then in USMF.</span></span>

<span data-ttu-id="7df5e-141">次の図は、計画製造オーダーの **複数レベルのペギング** ページで、この例がどのように表示されるかを示します。</span><span class="sxs-lookup"><span data-stu-id="7df5e-141">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![2 つの会社が関わる会社間の例](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a><span data-ttu-id="7df5e-143">3 つの会社が関わる会社間の例</span><span class="sxs-lookup"><span data-stu-id="7df5e-143">Intercompany example that involves three companies</span></span>

<span data-ttu-id="7df5e-144">この例では、USMF 会社で計画発注書を作成し、DEMF 会社で販売注文をカバーします。</span><span class="sxs-lookup"><span data-stu-id="7df5e-144">For this example, a planned purchase order is created in the USMF company to cover a sales order in the FRRT company.</span></span> <span data-ttu-id="7df5e-145">DEMF および USMF 会社では、直接需要は計画企業内需要です。</span><span class="sxs-lookup"><span data-stu-id="7df5e-145">In the DEMF and USMF companies, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="7df5e-146">この需要を USMF で表示するには、マスター プランをまず FRRT で実行してから DEMF で実行し、最後に USMF で実行します。</span><span class="sxs-lookup"><span data-stu-id="7df5e-146">To make this demand appear in USMF, master planning is run first in FRRT, then in DEMF, and finally in USMF.</span></span>

<span data-ttu-id="7df5e-147">次の図は、計画製造オーダーの **複数レベルのペギング** ページで、この例がどのように表示されるかを示します。</span><span class="sxs-lookup"><span data-stu-id="7df5e-147">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![3 つの会社が関わる会社間の例](media/IntercompanyPlanning2.png)
