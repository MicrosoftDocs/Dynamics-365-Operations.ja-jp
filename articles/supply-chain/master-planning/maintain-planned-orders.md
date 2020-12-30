---
title: 計画オーダーの管理
description: このトピックでは、計画オーダーの管理方法について説明します。 計画オーダーの状態の更新と確定、選択した計画オーダーとして同じ状態である計画オーダーをフィルター処理する方法について説明します。
author: roxanadiaconu
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f62381ca212e711fd61e12c9ec8f066ec124a933
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432203"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="05e0c-104">計画オーダーの管理</span><span class="sxs-lookup"><span data-stu-id="05e0c-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="05e0c-105">このトピックでは、計画オーダーの管理方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="05e0c-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="05e0c-106">計画オーダーの状態の更新と確定、選択した計画オーダーとして同じ状態である計画オーダーをフィルター処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="05e0c-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="05e0c-107">**マスター プラン** ワークスペース、**計画オーダー** リスト、または **計画製造オーダー**、**計画発注書**、および **計画移動** リストから計画オーダーを管理できます。</span><span class="sxs-lookup"><span data-stu-id="05e0c-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="05e0c-108">計画済オーダーのステータス</span><span class="sxs-lookup"><span data-stu-id="05e0c-108">Planned order status</span></span>
<span data-ttu-id="05e0c-109">**ステータス** フィールドを使用して、進捗状況を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="05e0c-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="05e0c-110">次の値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="05e0c-110">The following values are used:</span></span>

-   <span data-ttu-id="05e0c-111">マスター プランによって計画オーダーが生成されたとき、計画オーダーのステータスは **未処理** になります。</span><span class="sxs-lookup"><span data-stu-id="05e0c-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="05e0c-112">計画オーダーを確定しない場合は、ステータスを **完了済み** に設定できます。</span><span class="sxs-lookup"><span data-stu-id="05e0c-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="05e0c-113">計画済オーダーを確定する場合は、ステータスを **承認済** に変更できます。</span><span class="sxs-lookup"><span data-stu-id="05e0c-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="05e0c-114">**承認済** ステータスがある計画済オーダーは、マスター プランで尊重されるため、後でマスター プランの実行中に変更または削除されることはありません。</span><span class="sxs-lookup"><span data-stu-id="05e0c-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted during a later master planning run.</span></span> <span data-ttu-id="05e0c-115">これを達成するため、計画ロジックはマスター プラン中に、**承認済** 計画オーダーを古い計画バージョンから新しい計画バージョンにコピーします。</span><span class="sxs-lookup"><span data-stu-id="05e0c-115">To achieve this, the planning logic copies the **Approved** planned orders from the old plan version to the new plan version during master planning.</span></span>

## <a name="firming-planned-orders"></a><span data-ttu-id="05e0c-116">計画済オーダーの確定</span><span class="sxs-lookup"><span data-stu-id="05e0c-116">Firming planned orders</span></span> 
<span data-ttu-id="05e0c-117">計画済オーダーを確定することによって、実際の注文が作成されます。</span><span class="sxs-lookup"><span data-stu-id="05e0c-117">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="05e0c-118">これらは、*リリース済* または *オープン注文* とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="05e0c-118">These are also known as *released* or *open orders*.</span></span> <span data-ttu-id="05e0c-119">計画オーダーが確定されると、関連するモジュールの注文セクションにその計画オーダーが移動します。</span><span class="sxs-lookup"><span data-stu-id="05e0c-119">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="05e0c-120">**計画済オーダー** ページから、次の 2 つの確定オプションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="05e0c-120">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="05e0c-121">**確定** – これにより、選択した 1 つまたは複数の計画済オーダーが確定されます。</span><span class="sxs-lookup"><span data-stu-id="05e0c-121">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="05e0c-122">**全て確定** – フィルター内のすべての計画済オーダーが確定されます。</span><span class="sxs-lookup"><span data-stu-id="05e0c-122">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="05e0c-123">**全て確定** を使用すると、計画済オーダーを選択する必要がなく、フィルター内のすべての計画済オーダーが確定されます。</span><span class="sxs-lookup"><span data-stu-id="05e0c-123">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="05e0c-124">このオプションは、多数の計画済オーダーを確定する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="05e0c-124">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="05e0c-125">**計画済オーダー フォーム > 表示 > 確定履歴** の **確定履歴** から、確定された計画済オーダーを追跡できます。</span><span class="sxs-lookup"><span data-stu-id="05e0c-125">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="05e0c-126">確定並列化</span><span class="sxs-lookup"><span data-stu-id="05e0c-126">Parallelize firming</span></span>
<span data-ttu-id="05e0c-127">複数オーダーの同時確定を計画している場合は、実行を並列化することで、実行時間またはパフォーマンスを向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="05e0c-127">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="05e0c-128">このオプションは、**確定** または **全て確定** のいずれかで複数の計画済オーダーを確定する場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="05e0c-128">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="05e0c-129">次のパラメーターを使用できます。</span><span class="sxs-lookup"><span data-stu-id="05e0c-129">The following parameters are available:</span></span>

-   <span data-ttu-id="05e0c-130">**並列確定** – **はい** の場合、確定プロセスは、**スレッドの数** で定義されたスレッド数で並列処理されます。</span><span class="sxs-lookup"><span data-stu-id="05e0c-130">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="05e0c-131">**スレッドの数** – 確定プロセスを並列化するために、使用されるスレッドの数を制御します。</span><span class="sxs-lookup"><span data-stu-id="05e0c-131">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="05e0c-132">パラメーターは、**並列化の確定** が、**はい** に設定されている場合にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="05e0c-132">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>

> [!NOTE]
> <span data-ttu-id="05e0c-133">**確定並列化** のオプションは、確定のために複数の計画オーダーが選択されている場合にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="05e0c-133">The option for **Parallelize firming** is only shown when you have more than one planned order selected for firming.</span></span>

<a name="additional-resources"></a><span data-ttu-id="05e0c-134">追加リソース</span><span class="sxs-lookup"><span data-stu-id="05e0c-134">Additional resources</span></span>
--------

[<span data-ttu-id="05e0c-135">マスター プランの概要</span><span class="sxs-lookup"><span data-stu-id="05e0c-135">Master plans overview</span></span>](master-plans.md)



