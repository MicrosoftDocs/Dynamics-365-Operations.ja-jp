---
title: ミックス モードの計画 - ディスクリート、プロセス、およびリーン ソーシングを組み合わせる
description: このトピックは、ミックス モードの計画に関する情報を提供します。
author: cvocph
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 52931
ms.assetid: 2e8b5fd1-cee9-45da-a3ae-6961fb020b89
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 84a580ff6e8fe91de1ce0af315f322487dd8a3b2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814853"
---
# <a name="mixed-mode-planning---combine-discrete-process-and-lean-sourcing"></a><span data-ttu-id="b98eb-103">ミックス モードの計画 - ディスクリート、プロセス、およびリーン ソーシングを組み合わせる</span><span class="sxs-lookup"><span data-stu-id="b98eb-103">Mixed mode planning - Combine discrete, process, and lean sourcing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b98eb-104">このトピックは、ミックス モードの計画に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="b98eb-104">This topic provides information about mixed mode planning.</span></span> <span data-ttu-id="b98eb-105">ミックス モードの計画では、材料フローに基づいてサプライ チェーンをシミュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="b98eb-105">In mixed mode planning, you can model your supply chain based on the material flow.</span></span> <span data-ttu-id="b98eb-106">Dynamics 365 Supply Chain Management は、選択した供給ポリシー (かんばん、製造オーダー、発注書、バッチ オーダー、または移動オーダー) に関係なく、材料フローがモデルにならうことを確認します。</span><span class="sxs-lookup"><span data-stu-id="b98eb-106">Dynamics 365 Supply Chain Management makes sure that the material flow follows your models, regardless of the supply policy that is selected (kanbans, production orders, purchase orders, batch orders, or transfer orders).</span></span> 

<span data-ttu-id="b98eb-107">製品構造に関係なく製品を供給するための全体的な戦略を選択できます。</span><span class="sxs-lookup"><span data-stu-id="b98eb-107">You can select your overall strategy for supplying a product, regardless of the product structure.</span></span>  

<span data-ttu-id="b98eb-108">たとえば、組み立てにおけるかんばんのコントロールができます。製造オーダー、かんばん、転送、バッチ オーダー、または、サプライ チェーンの特性に適した任意の組み合わせにより組み立てエリアのために材料が供給されます。それでも、サプライ全体の可視性を保つことができます。</span><span class="sxs-lookup"><span data-stu-id="b98eb-108">For example, you can have kanban control in the assembly, where materials are sourced for the assembly area by production orders, kanbans, transfers, batch orders, or any combination that is appropriate for the characteristics of your supply chain, but you can still have full visibility across supplies.</span></span> <span data-ttu-id="b98eb-109">この機能は、サプライ チェーンのプロセスの最適化やサプライ チェーンの可視性の向上につながります。</span><span class="sxs-lookup"><span data-stu-id="b98eb-109">This capability leads to optimized supply chain processes and enhanced visibility into your supply chain.</span></span>  

<span data-ttu-id="b98eb-110">マスター スケジューリングに使用する供給ポリシーの精度は、補充分析コードとして有効にされている保管分析コードによって異なります。</span><span class="sxs-lookup"><span data-stu-id="b98eb-110">The granularity of the supply policies that are used in master scheduling depends on the storage dimensions that are enabled as coverage dimensions.</span></span> <span data-ttu-id="b98eb-111">さまざまなタイプの場所 (たとえば、異なる生産単位の生産フロアを分けたり、さまざまなタイプの材料や完成品の倉庫を分けたりすること) の補充および供給を制御するためのマスター スケジューリングを有効にするには、補充分析コードとしてサイトと倉庫を有効にすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b98eb-111">To enable master scheduling to control the replenishment and supply of different types of locations (for example, by separating the production floor for different production units, or by separating different types of material and finished goods warehouses), we recommend that you enable Site and Warehouse as coverage dimensions.</span></span> <span data-ttu-id="b98eb-112">または、補充分析コードとして倉庫を省くことができます。</span><span class="sxs-lookup"><span data-stu-id="b98eb-112">Alternatively, Warehouse can be omitted as a coverage dimension.</span></span> <span data-ttu-id="b98eb-113">このとき、高度な倉庫管理を使用している場合、倉庫内のすべての移動は倉庫の作業によって制御され、一方、倉庫間のすべての移動は引き取りかんばんによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="b98eb-113">In that case, when you use advanced warehouse management, all movements inside a warehouse are controlled by warehouse work, whereas all movements across warehouses can be controlled by withdrawal kanbans.</span></span>

## <a name="supply-policies"></a><span data-ttu-id="b98eb-114">供給ポリシー</span><span class="sxs-lookup"><span data-stu-id="b98eb-114">Supply policies</span></span>
<span data-ttu-id="b98eb-115">ミックス モード計画では、製品の供給方法や供給に基づく派生供給 (部品表 \[BOM\]からの品目の消費) の発行方法を制御します。</span><span class="sxs-lookup"><span data-stu-id="b98eb-115">Mixed mode planning controls how a product is supplied and, based on the supply, how derived requirements (consumption of items from a bill of materials \[BOM\]) are issued.</span></span> <span data-ttu-id="b98eb-116">注文タイプに基づいて、システムは自動的に要件にかなう材料を調達します。</span><span class="sxs-lookup"><span data-stu-id="b98eb-116">Based on the order type, the system automatically sources materials to match the requirements.</span></span>  

<span data-ttu-id="b98eb-117">供給ポリシーは、製品レベルで、または、要件にかなうあらゆる精度で定めることができます。</span><span class="sxs-lookup"><span data-stu-id="b98eb-117">Supply policies can be defined at the product level or at any granularity that supports your requirements.</span></span> <span data-ttu-id="b98eb-118">供給ポリシーの精度は、**既定の注文設定** ページで設定します。</span><span class="sxs-lookup"><span data-stu-id="b98eb-118">You define the granularity of supply policies on the **Default order settings** page.</span></span>  

<span data-ttu-id="b98eb-119">供給ポリシーは、製品、品目分析コード (コンフィギュレーション、色やサイズ)、サイト、また倉庫により制御されます。</span><span class="sxs-lookup"><span data-stu-id="b98eb-119">Supply policies can be controlled by product, item dimensions (configuration, color, and size), site, and warehouse.</span></span> <span data-ttu-id="b98eb-120">この設定は **品目の補充** ページで行います。</span><span class="sxs-lookup"><span data-stu-id="b98eb-120">This setup is done on the **Item coverage** page.</span></span>  

<span data-ttu-id="b98eb-121">既定の注文タイプは、マスター プランがどのような注文を生成するかを制御します。</span><span class="sxs-lookup"><span data-stu-id="b98eb-121">The default order type controls what order master planning generates.</span></span>  

<span data-ttu-id="b98eb-122">サプライ チェーンのシミュレーション設定に関係なく、Supply Chain Management では、供給ポリシーの組み合わせがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b98eb-122">Regardless of how the supply chain is modeled, Supply Chain Management supports your mix of supply policies.</span></span> <span data-ttu-id="b98eb-123">かんばんから提供される製造オーダーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="b98eb-123">You can have production orders that are sourced from kanbans.</span></span> <span data-ttu-id="b98eb-124">または、転送やかんばんにより供給される製品を必要とするバッチ オーダーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="b98eb-124">Alternatively, you can have a batch order that requires a product that is supplied by transfers or by kanbans.</span></span>  

<span data-ttu-id="b98eb-125">Supply Chain Management では、材料フローがモデルに従っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b98eb-125">Supply Chain Management makes sure that the material flow follows the model.</span></span>  

<span data-ttu-id="b98eb-126">材料のピッキングの倉庫は、供給ポリシーが定義されると、実行時間に動的に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="b98eb-126">The warehouse for picking material is assigned dynamically at run time, after the supply policy has been defined.</span></span>  

<span data-ttu-id="b98eb-127">通常、かんばんは有効期間が短いため、未来の日付で作成されることはありません。</span><span class="sxs-lookup"><span data-stu-id="b98eb-127">Typically, kanbans aren't created for future dates, because a kanban has a short life cycle.</span></span> <span data-ttu-id="b98eb-128">サプライ チェーンの完全な可視性を維持するために、「計画かんばん」という新たな計画のコンセプトを導入しました。派生した要求を計算したり、実際のかんばんが作成されるときに使用されるのと同じロジックに基づいて要件が指定されていることを保証する助けになります。</span><span class="sxs-lookup"><span data-stu-id="b98eb-128">To maintain full visibility into the supply chain, we have introduced the new planning concept of a “planned kanban,” which is used to calculate derived requirements and helps guarantee that the requirements are sourced based on the same logic that is used when the actual kanban is created.</span></span>  

<span data-ttu-id="b98eb-129">同じロジックは、他のすべての供給ポリシー タイプに見られます。</span><span class="sxs-lookup"><span data-stu-id="b98eb-129">The same logic is present for all other supply policy types.</span></span> <span data-ttu-id="b98eb-130">したがって、材料の長期計画は、生産と供給が承認された後に、実際の注文で実行されると想定する同じロジックに基づきます。</span><span class="sxs-lookup"><span data-stu-id="b98eb-130">Therefore, long-term materials planning is based on the same logic that you expect to run with the actual orders after production and supply are approved.</span></span>

## <a name="materials-allocation-cross-supply-policy--resource-consumption-on-boms"></a><span data-ttu-id="b98eb-131">供給ポリシー全体にわたる材料の配賦 – BOM のリソース消費</span><span class="sxs-lookup"><span data-stu-id="b98eb-131">Materials allocation cross-supply policy – Resource consumption on BOMs</span></span>
<span data-ttu-id="b98eb-132">リソース消費は重要な機能です。</span><span class="sxs-lookup"><span data-stu-id="b98eb-132">Resource consumption is an important functionality.</span></span> <span data-ttu-id="b98eb-133">リソース消費により、供給ポリシー (注文タイプ) に基づき材料のピッキングを行う倉庫を動的に選択することが可能になり、また、基本データの管理も容易になります。</span><span class="sxs-lookup"><span data-stu-id="b98eb-133">Resource consumption enables a warehouse for picking materials to be selected dynamically, based on the supply policy (order type), and also makes maintenance of base data easier.</span></span>  

<span data-ttu-id="b98eb-134">リソース消費には、材料のピッキングをする倉庫を製品の供給方法に基づいて割り当てることが必要です。</span><span class="sxs-lookup"><span data-stu-id="b98eb-134">Resource consumption requires that the warehouse that materials are picked from be assigned based on the way that the product is supplied.</span></span> <span data-ttu-id="b98eb-135">つまり、実行時にシステムが製造に使用するリソースを検索します。</span><span class="sxs-lookup"><span data-stu-id="b98eb-135">In other words, at run time, the system finds the resources that should be used for manufacturing.</span></span> <span data-ttu-id="b98eb-136">これらのリソースに基づいて、システムは、ピッキング倉庫を検出します。</span><span class="sxs-lookup"><span data-stu-id="b98eb-136">Based on those resources, the system then finds the picking warehouse.</span></span>  

<span data-ttu-id="b98eb-137">供給ポリシーに依存しない作業では、供給が変更されても BOM の情報を変更する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b98eb-137">For work that is independent of a supply policy, you don't have to change information on the BOM if the supply is changed.</span></span> <span data-ttu-id="b98eb-138">暫定的な変更のために、Supply Chain Management では、材料が正しい倉庫から調達されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b98eb-138">For ad-hoc changes, Supply Chain Management makes sure that materials are sourced from the right warehouse.</span></span>

## <a name="process-manufacturing--the-production-type"></a><span data-ttu-id="b98eb-139">プロセス製造 – 製造タイプ</span><span class="sxs-lookup"><span data-stu-id="b98eb-139">Process manufacturing – The production type</span></span>
<span data-ttu-id="b98eb-140">混合モードの完全な柔軟性を得るには、すべての製品に生産タイプ BOM を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b98eb-140">For full flexibility in mixed mode, we recommend that you use production type BOMs for all products.</span></span> <span data-ttu-id="b98eb-141">次に、製造指図、かんばん、転送指図、または購買発注を使用して製品を供給することができます。</span><span class="sxs-lookup"><span data-stu-id="b98eb-141">You can then use production orders, kanbans, transfer orders, or purchase orders to supply a product.</span></span> <span data-ttu-id="b98eb-142">プロセス製造では、**式**、**連産物**、**副産物**、または **計画品目** の製造タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="b98eb-142">For process manufacturing, you must use a production type of **Formula**, **Co-product**, **By-product**, or **Planning item**.</span></span> <span data-ttu-id="b98eb-143">かんばんと製造オーダーは、これらの生産タイプでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="b98eb-143">Kanbans and production orders can't be used for these production types.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]