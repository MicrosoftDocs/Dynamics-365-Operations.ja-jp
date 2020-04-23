---
title: 遅延
description: このトピックは、マスタ プランの遅延日に関する情報を提供します。 遅延日は、マスター プランで計算される最も早い履行日が、要求日より後になる場合にトランザクションに設定される現実的な期日です。
author: roxanadiaconu
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34252e5cd9ee5151b1cba47975fc0cc612521a17
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203851"
---
# <a name="delays"></a><span data-ttu-id="b1e48-104">遅延</span><span class="sxs-lookup"><span data-stu-id="b1e48-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1e48-105">このトピックは、マスタ プランの遅延日に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="b1e48-105">This topic provides information about delayed dates in master planning.</span></span> <span data-ttu-id="b1e48-106">遅延日は、マスター プランで計算される最も早い履行日が、要求日より後になる場合にトランザクションに設定される現実的な期日です。</span><span class="sxs-lookup"><span data-stu-id="b1e48-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="b1e48-107">マスター プランでは、リード タイム、材料の可用性、能力の利用可能性、計画のさまざまなパラメーターに基づいて、トランザクションの最も早い履行日を計算できます。</span><span class="sxs-lookup"><span data-stu-id="b1e48-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="b1e48-108">マスター プランの計算で現在の日付より前の注文日付になった場合、注文を時間どおりに履行することはできません。</span><span class="sxs-lookup"><span data-stu-id="b1e48-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="b1e48-109">したがって、注文は遅延します。</span><span class="sxs-lookup"><span data-stu-id="b1e48-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="b1e48-110">この場合、マスター プランは、現在の日付からフォワード プランニングを行い、注文リード タイムを含むようにします。</span><span class="sxs-lookup"><span data-stu-id="b1e48-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="b1e48-111">これらのリード タイムは、任意の下位レベルのコンポーネント品目から開始されます。</span><span class="sxs-lookup"><span data-stu-id="b1e48-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="b1e48-112">その後、注文は、遅延日付を与えられます。</span><span class="sxs-lookup"><span data-stu-id="b1e48-112">The order then receives a delayed date.</span></span> <span data-ttu-id="b1e48-113">遅延日は、現在のデータに基づく実際的な期日です。</span><span class="sxs-lookup"><span data-stu-id="b1e48-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="b1e48-114">マスター プランは、遅延日数の計算も行います。</span><span class="sxs-lookup"><span data-stu-id="b1e48-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="b1e48-115">代替の荷渡方法を選択してリード タイムを短縮できることをユーザーがわかっている場合など、状況によっては遅延を計算しないように選択することがあります。</span><span class="sxs-lookup"><span data-stu-id="b1e48-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="b1e48-116">補充グループに対して、遅延の計算方法を設定できます。</span><span class="sxs-lookup"><span data-stu-id="b1e48-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="b1e48-117">その後、補充グループを品目に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="b1e48-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="b1e48-118">**マスター プランのパラメーター**ページで、遅延計算の開始時刻を設定できます。</span><span class="sxs-lookup"><span data-stu-id="b1e48-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="b1e48-119">この時刻以降に注文を履行する場合、注文の遅延日に 1 日が追加されます。</span><span class="sxs-lookup"><span data-stu-id="b1e48-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

> [!NOTE]
> <span data-ttu-id="b1e48-120">注記 : 以前のバージョンでは、計算済遅延は*計画メッセージ*、遅延日は*計画期日*、遅延トランザクションは*計画設定済のトランザクション*と呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="b1e48-120">In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

## <a name="limited-delays-in-production-setup-with-multiple-bom-levels"></a><span data-ttu-id="b1e48-121">複数の BOM レベルを使用した生産設定の遅延の制限</span><span class="sxs-lookup"><span data-stu-id="b1e48-121">Limited delays in production setup with multiple BOM levels</span></span>
<span data-ttu-id="b1e48-122">複数の BOM レベルがある生産設定で遅延を処理する場合、遅延を発生させた (BOM 構造内の) 品目のすぐ上の品目のみに、マスター プランの実行の一部として遅延付きで更新されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b1e48-122">When you work with delays in a production setup that has multiple BOM levels, it is important to note that only the items directly above the item (in the BOM structure) causing the delay, will be updated with a delay as part of the master planning run.</span></span> <span data-ttu-id="b1e48-123">BOM 構造の他の品目には、最上位レベルの計画オーダーが承認または確定された場合、最初のマスター プランの実行まで、遅延は適用されません。</span><span class="sxs-lookup"><span data-stu-id="b1e48-123">Other items in the BOM structure will not get the delay applied until the first master planning run, when the planned order for the top level is approved or firmed.</span></span> 

<span data-ttu-id="b1e48-124">この既知の制限を回避するために、遅延のある BOM 構造の上位にある製造オーダーを、次のマスター プランの実行前に承認 (または確定) できます。</span><span class="sxs-lookup"><span data-stu-id="b1e48-124">To work around this known limitation, the production orders on the top of the BOM structure with delays can be approved (or firmed) prior to the next master planning run.</span></span> <span data-ttu-id="b1e48-125">これにより、遅延承認済み計画製造オーダーからの遅延が保持され、すべての基になるコンポーネントがそれに応じて更新されます。</span><span class="sxs-lookup"><span data-stu-id="b1e48-125">This way the delay from the delayed approved planned production order will be kept and all underlying components will be updated accordingly.</span></span>
<span data-ttu-id="b1e48-126">アクション メッセージ、BOM 構造の他の遅延が原因で、後の日付に移動できる計画オーダーを識別するためにも使用できます。</span><span class="sxs-lookup"><span data-stu-id="b1e48-126">Action messages can also be used to identify planned orders that can be moved to a later date, due to other delays in the BOM structure.</span></span>

## <a name="desired-date"></a><span data-ttu-id="b1e48-127">納入希望日</span><span class="sxs-lookup"><span data-stu-id="b1e48-127">Desired date</span></span>

<span data-ttu-id="b1e48-128">**遅延**タブの下の**計画済オーダー**ページは、計画済オーダーの**希望日**です。</span><span class="sxs-lookup"><span data-stu-id="b1e48-128">On the **Planned order** page, under the **Delays** tab is the **Desired date** for the planned order.</span></span> <span data-ttu-id="b1e48-129">計画済オーダーの希望日は遅延の基本日となり、**正味必要量**から計算された**希望日**に等しい計算日です。</span><span class="sxs-lookup"><span data-stu-id="b1e48-129">The desired date of a planned order is the base date for delays, which is a computed date that equals the **Requested date** calculated from the **Net Requirement**.</span></span> <span data-ttu-id="b1e48-130">計画済オーダーが BOM 明細行、生産明細行またはかんばん明細行の場合、目的の日付は**要求日**に基づいて要求され、**計画済オーダー**ページには表示されません。</span><span class="sxs-lookup"><span data-stu-id="b1e48-130">If the planned order is a BOM line, production line or kanban line, the desired date is based on the **Requirement date** and the desired date will not be shown on the **Planned order** page.</span></span>

<a name="additional-resources"></a><span data-ttu-id="b1e48-131">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b1e48-131">Additional resources</span></span>
--------

[<span data-ttu-id="b1e48-132">補充設定</span><span class="sxs-lookup"><span data-stu-id="b1e48-132">Coverage settings</span></span>](coverage-settings.md)
