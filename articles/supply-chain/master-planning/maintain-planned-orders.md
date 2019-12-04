---
title: 計画オーダーの管理
description: このトピックでは、計画オーダーの管理方法について説明します。 計画オーダーの状態の更新と確定、選択した計画オーダーとして同じ状態である計画オーダーをフィルター処理する方法について説明します。
author: roxanadiaconu
manager: AnnBe
ms.date: 11/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68bccb632255eac975dc150cf322d4c579ff2f24
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813779"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="3f857-104">計画オーダーの管理</span><span class="sxs-lookup"><span data-stu-id="3f857-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f857-105">このトピックでは、計画オーダーの管理方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3f857-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="3f857-106">計画オーダーの状態の更新と確定、選択した計画オーダーとして同じ状態である計画オーダーをフィルター処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3f857-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="3f857-107">**マスター プラン** ワークスペース、**計画オーダー** リスト、または**計画製造オーダー**、**計画発注書**、および**計画移動**リストから計画オーダーを管理できます。</span><span class="sxs-lookup"><span data-stu-id="3f857-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="3f857-108">計画済オーダーのステータス</span><span class="sxs-lookup"><span data-stu-id="3f857-108">Planned order status</span></span>
<span data-ttu-id="3f857-109">**ステータス** フィールドを使用して、進捗状況を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="3f857-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="3f857-110">次の値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f857-110">The following values are used:</span></span>

-   <span data-ttu-id="3f857-111">マスター プランによって計画オーダーが生成されたとき、計画オーダーのステータスは **未処理** になります。</span><span class="sxs-lookup"><span data-stu-id="3f857-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="3f857-112">計画オーダーを確定しない場合は、ステータスを **完了済み** に設定できます。</span><span class="sxs-lookup"><span data-stu-id="3f857-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="3f857-113">計画済オーダーを確定する場合は、ステータスを**承認済**に変更できます。</span><span class="sxs-lookup"><span data-stu-id="3f857-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="3f857-114">**承認済**ステータスがある計画済オーダーは、マスター プランで尊重されるため、後でマスター プランの実行中に変更または削除されることはありません。</span><span class="sxs-lookup"><span data-stu-id="3f857-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted during a later master planning run.</span></span> 

## <a name="firming-planned-orders"></a><span data-ttu-id="3f857-115">計画済オーダーの確定</span><span class="sxs-lookup"><span data-stu-id="3f857-115">Firming planned orders</span></span> 
<span data-ttu-id="3f857-116">計画済オーダーを確定することによって、実際の注文が作成されます。</span><span class="sxs-lookup"><span data-stu-id="3f857-116">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="3f857-117">これらは、*リリース済*または*オープン注文*としても認識されます。</span><span class="sxs-lookup"><span data-stu-id="3f857-117">These are also know as *released* or *open orders*.</span></span> <span data-ttu-id="3f857-118">計画オーダーが確定されると、関連するモジュールの注文セクションにその計画オーダーが移動します。</span><span class="sxs-lookup"><span data-stu-id="3f857-118">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="3f857-119">**計画済オーダー**ページから、次の 2 つの確定オプションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="3f857-119">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="3f857-120">**確定** – これにより、選択した 1 つまたは複数の計画済オーダーが確定されます。</span><span class="sxs-lookup"><span data-stu-id="3f857-120">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="3f857-121">**全て確定** – フィルター内のすべての計画済オーダーが確定されます。</span><span class="sxs-lookup"><span data-stu-id="3f857-121">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="3f857-122">**全て確定**を使用すると、計画済オーダーを選択する必要がなく、フィルター内のすべての計画済オーダーが確定されます。</span><span class="sxs-lookup"><span data-stu-id="3f857-122">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="3f857-123">このオプションは、多数の計画済オーダーを確定する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="3f857-123">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="3f857-124">**計画済オーダー フォーム > 表示 > 確定履歴**の**確定履歴**から、確定された計画済オーダーを追跡できます。</span><span class="sxs-lookup"><span data-stu-id="3f857-124">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="3f857-125">確定並列化</span><span class="sxs-lookup"><span data-stu-id="3f857-125">Parallelize firming</span></span>
<span data-ttu-id="3f857-126">複数オーダーの同時確定を計画している場合は、実行を並列化することで、実行時間またはパフォーマンスを向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="3f857-126">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="3f857-127">このオプションは、**確定**または**全て確定**のいずれかで複数の計画済オーダーを確定する場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="3f857-127">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="3f857-128">次のパラメーターを使用できます。</span><span class="sxs-lookup"><span data-stu-id="3f857-128">The following parameters are available:</span></span>

-   <span data-ttu-id="3f857-129">**並列確定** – **はい**の場合、確定プロセスは、**スレッドの数**で定義されたスレッド数で並列処理されます。</span><span class="sxs-lookup"><span data-stu-id="3f857-129">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="3f857-130">**スレッドの数** – 確定プロセスを並列化するために、使用されるスレッドの数を制御します。</span><span class="sxs-lookup"><span data-stu-id="3f857-130">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="3f857-131">パラメーターは、**並列化の確定**が、**はい**に設定されている場合にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="3f857-131">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>


<a name="additional-resources"></a><span data-ttu-id="3f857-132">追加リソース</span><span class="sxs-lookup"><span data-stu-id="3f857-132">Additional resources</span></span>
--------

[<span data-ttu-id="3f857-133">マスター プランの概要</span><span class="sxs-lookup"><span data-stu-id="3f857-133">Master plans overview</span></span>](master-plans.md)



