---
title: "製造オーダーのリリース"
description: "リリースされた製造オーダーは、生産が承認された注文です。 生産の作業現場と倉庫でのプロセス実行に使用でき製造オーダーには、製造オーダーのライフ サイクルの状態を説明するのに \"リリース済\" という語句が使用されます。"
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f45aa9448837ee9588f9f9ba4593bf7c3f2e7954
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="release-production-orders"></a><span data-ttu-id="6f547-104">製造オーダーのリリース</span><span class="sxs-lookup"><span data-stu-id="6f547-104">Release production orders</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="6f547-105">リリースされた製造オーダーは、生産が承認された注文です。</span><span class="sxs-lookup"><span data-stu-id="6f547-105">A released production order is an order that has been authorized for production.</span></span> <span data-ttu-id="6f547-106">生産の作業現場と倉庫でのプロセス実行に使用でき製造オーダーには、製造オーダーのライフ サイクルの状態を説明するのに "リリース済" という語句が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6f547-106">The term Released is used to describe a state in the production order life cycle, where the production order is available for execution on the production shop floor and for warehouse processes.</span></span> 

<a name="characteristics-of-the-released-state"></a><span data-ttu-id="6f547-107">リリース済ステータスの特性</span><span class="sxs-lookup"><span data-stu-id="6f547-107">Characteristics of the Released state</span></span>
-------------------------------------

<span data-ttu-id="6f547-108">**リリース済**ステータスは、製造オーダーのライフ サイクルの 1 つの状態です。</span><span class="sxs-lookup"><span data-stu-id="6f547-108">The **Released** state is one state in the production order life cycle.</span></span> <span data-ttu-id="6f547-109">**リリース済**状態にある製造オーダーは、生産の作業現場と倉庫でのプロセス実行に使用できます。</span><span class="sxs-lookup"><span data-stu-id="6f547-109">Production orders that are in the **Released** state are available for execution on the production shop floor and for warehouse processes.</span></span> <span data-ttu-id="6f547-110">**リリース済**ステータスは次の特徴があります。</span><span class="sxs-lookup"><span data-stu-id="6f547-110">The **Released** state has the following characteristics:</span></span>

-   <span data-ttu-id="6f547-111">製造オーダーは、製造オーダーから、またはバッチ処理を使用して、**リリース済**ステータスに変更できます。</span><span class="sxs-lookup"><span data-stu-id="6f547-111">A production order can be changed to the **Released** state either from the production order or by using a batch process.</span></span> <span data-ttu-id="6f547-112">また、製造オーダーは、**マスター プラン** ページの**確定タイム フェンス** フィールドを使用して確定される計画製造オーダーにより、自動的に更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="6f547-112">The production order can also be updated automatically from planned production orders that are firmed by using the **Firming time fence** field on the **Master plan** page.</span></span>
-   <span data-ttu-id="6f547-113">**リリース済**ステータスは、作業現場の操作員に、作業現場での生産ジョブの実行を開始してもらうための合図です。</span><span class="sxs-lookup"><span data-stu-id="6f547-113">The **Released** state is the signal for the shop floor operators (operators) to start executing the production jobs on the shop floor.</span></span>
-   <span data-ttu-id="6f547-114">工順カード、工順ジョブ、ジョブ カードなど、生産ジョブについての情報を提供する生産文書を発行することができます。</span><span class="sxs-lookup"><span data-stu-id="6f547-114">Production papers, such as route cards, route jobs, and jobs cards provide information about production jobs and can be issued.</span></span>
-   <span data-ttu-id="6f547-115">現物引当済である材料の場合、倉庫の作業が生成され、製造オーダーに対する材料のピッキングを行います。</span><span class="sxs-lookup"><span data-stu-id="6f547-115">For materials that are physically reserved, warehouse work is generated to pick materials for the production order.</span></span>

## <a name="releasing-jobs-to-the-shop-floor"></a><span data-ttu-id="6f547-116">作業現場へのジョブのリリース</span><span class="sxs-lookup"><span data-stu-id="6f547-116">Releasing jobs to the shop floor</span></span>
<span data-ttu-id="6f547-117">製造オーダーがリリースされた後、注文に関連付けられる生産ジョブが表示され、登録が実行できるようになります。</span><span class="sxs-lookup"><span data-stu-id="6f547-117">After a production order is released, production jobs that are related to the order are visible and ready for registration.</span></span> <span data-ttu-id="6f547-118">操作員は、[**ジョブ カード ターミナル**] ページまたは [**ジョブ カード デバイス**] ページのいずれかで、開始、停止、完了などのジョブ登録を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="6f547-118">The operators can make job registrations, such as Start, Stop, and Completion, on either the **Job card terminal** page or the **Job card device** page.</span></span> <span data-ttu-id="6f547-119">登録された時間と数量は、登録ページから生産仕訳帳に自動的に転送され、消費時間と数量が記録されます。</span><span class="sxs-lookup"><span data-stu-id="6f547-119">The registered time and quantity are automatically transferred from the registration pages to production journals to keep track of the consumed time and quantity.</span></span>

## <a name="route-cards"></a><span data-ttu-id="6f547-120">工順カード</span><span class="sxs-lookup"><span data-stu-id="6f547-120">Route cards</span></span>
<span data-ttu-id="6f547-121">工順カードには、工順と工程の設定から、および開始工程とジョブのスケジュール方法から取得された情報の概要が記載されます。</span><span class="sxs-lookup"><span data-stu-id="6f547-121">A route card provides an overview of information that comes from route and operation setups, and from operation and job scheduling methods.</span></span>

## <a name="route-jobs"></a><span data-ttu-id="6f547-122">工順ジョブ</span><span class="sxs-lookup"><span data-stu-id="6f547-122">Route jobs</span></span>
<span data-ttu-id="6f547-123">工順ジョブには工程の各ジョブの詳細が一覧表示され、段取り時間、処理時間、待ち時間、配送時間などが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6f547-123">A route job lists each job of an operation in detail, and includes setup, process, queue, and transportation times.</span></span> <span data-ttu-id="6f547-124">たとえば、塗装などの工程では、段取り時間、塗装プロセスの実行時間、塗装が乾くまでの待ち時間などの、個々のジョブが必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="6f547-124">For example, an operation such as painting might require individual jobs, such as setup time, run time for the painting process, and queue time for drying.</span></span>

## <a name="job-cards"></a><span data-ttu-id="6f547-125">ジョブ カード</span><span class="sxs-lookup"><span data-stu-id="6f547-125">Job cards</span></span>
<span data-ttu-id="6f547-126">ジョブ カードには、特定の工程を示す個々のジョブ番号が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="6f547-126">A job card lists the individual job numbers of a particular operation.</span></span> <span data-ttu-id="6f547-127">各ページに 1 種類のジョブが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6f547-127">One job appears on each page.</span></span> <span data-ttu-id="6f547-128">ジョブ カードに含まれるジョブとその見積時間は、工順および工程の設定情報から取得されます。</span><span class="sxs-lookup"><span data-stu-id="6f547-128">The jobs that are included on a job card, and their estimated times, come from the route and operation setup information.</span></span> <span data-ttu-id="6f547-129">ジョブ カードから、**生産仕訳帳明細行**、**ジョブ カード** ページを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="6f547-129">From a job card, you can open the **Production journal lines**, **job card** page.</span></span> <span data-ttu-id="6f547-130">運営リソースの運用担当者は、生産プロセスに関するフィードバックを提供できます。</span><span class="sxs-lookup"><span data-stu-id="6f547-130">People who run operations resources can provide feedback about the production process.</span></span> <span data-ttu-id="6f547-131">消費統計や、エラー数量などの情報を入力できるフィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="6f547-131">There are fields where you can enter consumption statistics and information such as the error quantity.</span></span>

## <a name="warehouse-work-for-raw-material-picking"></a><span data-ttu-id="6f547-132">原材料ピッキングの倉庫作業</span><span class="sxs-lookup"><span data-stu-id="6f547-132">Warehouse work for raw material picking</span></span>
<span data-ttu-id="6f547-133">原材料ピッキングの作業がリリース時に生成されます。</span><span class="sxs-lookup"><span data-stu-id="6f547-133">Work for raw material picking is generated during release.</span></span> <span data-ttu-id="6f547-134">注文がリリースされる前に、製造オーダーのために引当された現物品目の数量に対してのみ作業が生成されます。</span><span class="sxs-lookup"><span data-stu-id="6f547-134">Work is generated only for the quantity of materials that was physically reserved for the production order before the order was released.</span></span> <span data-ttu-id="6f547-135">原材料ピッキングの倉庫作業を生成するには、以下の設定が必要です。</span><span class="sxs-lookup"><span data-stu-id="6f547-135">The following setup is required to generate warehouse work for raw material picking:</span></span>

-   <span data-ttu-id="6f547-136">材料をピッキングする倉庫の場所を決定する、原材料ピッキングの場所のディレクティブ</span><span class="sxs-lookup"><span data-stu-id="6f547-136">A location directive for raw materials picking that determines which warehouse location to pick the materials in</span></span>
-   <span data-ttu-id="6f547-137">倉庫作業の実行ポリシーを構成する、原材料のウェーブ テンプレート</span><span class="sxs-lookup"><span data-stu-id="6f547-137">A wave template for raw materials, where policies for the execution of warehouse work are configured</span></span>
-   <span data-ttu-id="6f547-138">材料をプットする場所を決定する、生産入庫の場所</span><span class="sxs-lookup"><span data-stu-id="6f547-138">A production input location that determines where materials are put</span></span>





