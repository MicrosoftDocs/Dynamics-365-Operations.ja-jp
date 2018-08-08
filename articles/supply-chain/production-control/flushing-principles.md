---
title: "部品消費ルール"
description: "このトピックでは、原材料消費に使用される次の 4 つの部品消費ルールについて説明します。"
author: johanhoffmann
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgShopSupervisorReleaseOrders
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: e4b9cd918bec9a094744b208821285c57f01798a
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---

# <a name="controlling-raw-material-consumption-by-using-flushing-principles"></a><span data-ttu-id="f8d3e-103">消費ルールを使用して原材料消費を管理する</span><span class="sxs-lookup"><span data-stu-id="f8d3e-103">Controlling raw material consumption by using flushing principles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8d3e-104">部品消費ルールは、生産プロセスで使用される原材料における消費戦略とは異なる戦略を反映します。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-104">The flushing principles reflect different consumption strategies for raw materials that are used in production processes.</span></span> <span data-ttu-id="f8d3e-105">消費は、手持在庫から品目を差し引き、消費品目の金額を、製造オーダーおよびバッチ オーダーの**進行中の作業** (WIP) に設定するプロセスです。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-105">Consumption is the process that deducts material from the on-hand inventory and sets the value of the consumed materials to **Work in progress** (WIP) for production orders and batch orders.</span></span> <span data-ttu-id="f8d3e-106">通常、原材料は、材料を消費するプロセスで構成されている場所から消費されます。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-106">Raw materials are usually consumed from a location that is configured for the process that consumes the material.</span></span> <span data-ttu-id="f8d3e-107">この場所は、生産入庫の場所と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-107">This location is known as the production input location.</span></span>

<span data-ttu-id="f8d3e-108">材料消費の前に、材料は、入庫場所に移動されます。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-108">Before material consumption, the materials are moved to the input location.</span></span> <span data-ttu-id="f8d3e-109">次の図がプロセスを示します。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-109">The following illustration shows the process.</span></span>

<span data-ttu-id="f8d3e-110">[![scenario4a](./media/scenario4a.png)](./media/scenario4a.png)</span><span class="sxs-lookup"><span data-stu-id="f8d3e-110">[![scenario4a](./media/scenario4a.png)](./media/scenario4a.png)</span></span>

1. <span data-ttu-id="f8d3e-111">材料倉庫</span><span class="sxs-lookup"><span data-stu-id="f8d3e-111">Material warehouse</span></span>
2. <span data-ttu-id="f8d3e-112">原材料のピッキング</span><span class="sxs-lookup"><span data-stu-id="f8d3e-112">Raw material picking</span></span>
3. <span data-ttu-id="f8d3e-113">生産入庫の場所</span><span class="sxs-lookup"><span data-stu-id="f8d3e-113">Production input location</span></span>
4. <span data-ttu-id="f8d3e-114">原材料消費</span><span class="sxs-lookup"><span data-stu-id="f8d3e-114">Raw material consumption</span></span>
5. <span data-ttu-id="f8d3e-115">生産プロセス</span><span class="sxs-lookup"><span data-stu-id="f8d3e-115">Production process</span></span>

<span data-ttu-id="f8d3e-116">材料消費は、次の 4 つの部品消費ルールによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-116">Material consumption is controlled by the following four flushing principles:</span></span>

- <span data-ttu-id="f8d3e-117">手動</span><span class="sxs-lookup"><span data-stu-id="f8d3e-117">Manual</span></span>
- <span data-ttu-id="f8d3e-118">開始</span><span class="sxs-lookup"><span data-stu-id="f8d3e-118">Start</span></span>
- <span data-ttu-id="f8d3e-119">完了</span><span class="sxs-lookup"><span data-stu-id="f8d3e-119">Finish</span></span>
- <span data-ttu-id="f8d3e-120">[場所で利用可能]</span><span class="sxs-lookup"><span data-stu-id="f8d3e-120">Available at location</span></span>

<span data-ttu-id="f8d3e-121">部品消費ルールは、既定値の階層で構成されます。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-121">The flushing principles are configured in a hierarchy of default values.</span></span> <span data-ttu-id="f8d3e-122">階層には、部品消費ルールが**開始**という値を持つリリース済の製品から始まります。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-122">The hierarchy starts at the released product, where the flushing principle has the value **Start**.</span></span> <span data-ttu-id="f8d3e-123">部品表 (BOM) またはフォーミュラ明細行には、製品から部品消費ルールを上書きできます。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-123">On the bill of materials (BOM) or formula line, the flushing principle from the product can be overridden.</span></span> <span data-ttu-id="f8d3e-124">生産 BOM 明細行またはバッチ オーダーのフォーミュラ明細行での既定部品消費ルールは、製品または BOM またはフォーミュラの上書きされた値から取得されます。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-124">The default flushing principle on the production BOM lines or batch order formula lines is taken from the product or the overridden value on the BOM or formulas.</span></span>

## <a name="description-of-the-flushing-principles"></a><span data-ttu-id="f8d3e-125">部品消費ルールの説明</span><span class="sxs-lookup"><span data-stu-id="f8d3e-125">Description of the flushing principles</span></span>

### <a name="manual"></a><span data-ttu-id="f8d3e-126">手動</span><span class="sxs-lookup"><span data-stu-id="f8d3e-126">Manual</span></span>
<span data-ttu-id="f8d3e-127">手動部品消費ルールは、材料消費の登録が手動操作であることを示します。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-127">The Manual flushing principle indicates that the registration of material consumption is a manual operation.</span></span> <span data-ttu-id="f8d3e-128">このルールは、追跡の目的で、時間を追跡できるようにしたい場合や、バッチ番号やシリアル番号の使用量を考慮する必要がある場合などに適しています。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-128">This principle is relevant if, for example, you want to be able to track time, and the quantity of consumed batch numbers or serial numbers must be accounted for, for tracking purposes.</span></span> <span data-ttu-id="f8d3e-129">手動の消費は、生産のピッキング リスト仕訳帳に登録されます。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-129">Manual consumption is registered in a production picking list journal.</span></span> <span data-ttu-id="f8d3e-130">高度な倉庫プロセスが有効になっている品目については、ハンドヘルド フローを適用できます。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-130">For items that are enabled for advanced warehouse processes, a hand-held flow can be applied.</span></span>

### <a name="start"></a><span data-ttu-id="f8d3e-131">開始</span><span class="sxs-lookup"><span data-stu-id="f8d3e-131">Start</span></span>
<span data-ttu-id="f8d3e-132">開始の部品消費ルールは、製造オーダーの開始時に品目が自動的に消費されることを示します。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-132">The Start flushing principle indicates that material will be automatically consumed when the production order is started.</span></span> <span data-ttu-id="f8d3e-133">消費される材料の量は、開始されている数量に比例します。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-133">The amount of material that is consumed is proportional to the quantity that is started.</span></span> <span data-ttu-id="f8d3e-134">開始の部品消費ルールを製造実行システムとともに使用すると、操作またはプロセス ジョブの開始時に材料をフラッシュすることもできます。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-134">When the Start flushing principle is used together with the manufacturing execution system, it can also be used to flush materials when an operation or a process job is started.</span></span> <span data-ttu-id="f8d3e-135">消費差異が低い、材料が低価額材料、追跡の要件がない、または操作における実行時間が短い場合は、このルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-135">This principle is relevant if, for example, the variance in the consumption is low, the materials are low-value materials, there are no tracking requirements, or there is a short run time on operations.</span></span> 

### <a name="finish"></a><span data-ttu-id="f8d3e-136">完了</span><span class="sxs-lookup"><span data-stu-id="f8d3e-136">Finish</span></span>
<span data-ttu-id="f8d3e-137">終了の部品消費ルールは、製造オーダーが終了したとき、または品目を消費するように設定された作業が完了した時点で登録されたときに品目が自動的に消費されることを示します。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-137">The Finish flushing principle indicates that material will be automatically consumed when the production order is reported as finished, or when an operation that is set up to consume the materials is registered as completed.</span></span> <span data-ttu-id="f8d3e-138">消費される材料の量は、終了と報告されている数量に比例します。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-138">The amount of material that is consumed is proportional to the quantity that is reported as finished.</span></span> <span data-ttu-id="f8d3e-139">終了の部品消費ルールを製造実行システムとともに使用すると、操作またはプロセス ジョブの完了時に材料をフラッシュすることもできます。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-139">When the Finish flushing principle is used together with the manufacturing execution system, it can also be used to flush materials when an operation or a process job is completed.</span></span> <span data-ttu-id="f8d3e-140">このルールは、開始ルールと同様の状況下で適用されます。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-140">This principle is relevant in the same situations as the Start principle.</span></span> <span data-ttu-id="f8d3e-141">ただし、終了ルールは実行時間が長い作業に適用されるため、作業が完了する前に品目を WIP に設定できません。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-141">However, the Finish principle is for operations that have a longer run time, where materials should not be set to WIP before the operation is completed.</span></span> 

### <a name="available-at-location"></a><span data-ttu-id="f8d3e-142">[場所で利用可能]</span><span class="sxs-lookup"><span data-stu-id="f8d3e-142">Available at location</span></span>
<span data-ttu-id="f8d3e-143">[場所別に利用可能] 部品消費ルールは、材料が生産のためにピッキングされたときに自動的に消費されることを示します。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-143">The Available at location flushing principle indicates that the material will be automatically consumed when it's registered as picked for production.</span></span> <span data-ttu-id="f8d3e-144">材料は、作業時間の原材料消費のピッキングが完了する、または生産入庫場所で品目が利用可能で、品目明細行が倉庫にリリースされると、在庫場所からピッキング済と登録されます。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-144">The material is registered as picked from location when work for the raw material picking is completed, or when material is available on the production input location and the material line is released to the warehouse.</span></span> <span data-ttu-id="f8d3e-145">プロセス中に生成されたピッキング リストは、バッチ ジョブで転記されます。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-145">The picking list that is generated during the process is posted in a batch job.</span></span> <span data-ttu-id="f8d3e-146">このルールは、たとえば、1 つの製造オーダーに対して多数のピッキング アクティビティがある場合に有効です。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-146">This principle is relevant if, for example, you have many picking activities against one production order.</span></span> <span data-ttu-id="f8d3e-147">この場合は、ピッキング リストを手動で更新する必要はありません。仕掛品残高の現在のビューを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="f8d3e-147">In this case, you don't have to update the picking list manually, and you can get a current view of the WIP balance.</span></span>

