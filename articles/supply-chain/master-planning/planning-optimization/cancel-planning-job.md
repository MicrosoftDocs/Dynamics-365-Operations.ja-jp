---
title: 計画ジョブのキャンセル
description: このトピックでは、計画の最適化機能を使用する有効な計画ジョブを取り消す方法について説明します。
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: a2d90f04985fdd66ca83582ee676100fffb26981
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774000"
---
[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

# <a name="cancel-a-planning-job"></a><span data-ttu-id="2e5e9-103">計画ジョブのキャンセル</span><span class="sxs-lookup"><span data-stu-id="2e5e9-103">Cancel a planning job</span></span>

<span data-ttu-id="2e5e9-104">Microsoft Dynamics 365 Supply Chain Management では、計画の最適化機能を使用する有効な計画ジョブを取り消す方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2e5e9-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning Optimization functionality.</span></span>

<span data-ttu-id="2e5e9-105">有効な計画ジョブをキャンセルするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="2e5e9-105">To cancel an active planning job, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="2e5e9-106">有効なジョブのみキャンセルすることができます。</span><span class="sxs-lookup"><span data-stu-id="2e5e9-106">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="2e5e9-107">**マスタープラン \> 設定 \> 計画**に移動します。</span><span class="sxs-lookup"><span data-stu-id="2e5e9-107">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="2e5e9-108">計画実行に適切な計画を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e5e9-108">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="2e5e9-109">**履歴**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e5e9-109">Select **History**.</span></span>
4. <span data-ttu-id="2e5e9-110">キャンセルする計画ジョブの選択</span><span class="sxs-lookup"><span data-stu-id="2e5e9-110">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="2e5e9-111">**キャンセル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e5e9-111">Select **Cancel**.</span></span>

<span data-ttu-id="2e5e9-112">ジョブ状態は、計画の最適化サービスがジョブのキャンセルを確認するまで**キャンセル中**になります。</span><span class="sxs-lookup"><span data-stu-id="2e5e9-112">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="2e5e9-113">その後、状態は**キャンセル済**に変更されます。</span><span class="sxs-lookup"><span data-stu-id="2e5e9-113">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="2e5e9-114">状態の変更を確認するには、**更新**ボタンを選択してページを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e5e9-114">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="related-resources"></a><span data-ttu-id="2e5e9-115">関連するリソース</span><span class="sxs-lookup"><span data-stu-id="2e5e9-115">Related resources</span></span>

[<span data-ttu-id="2e5e9-116">計画の最適化の概要</span><span class="sxs-lookup"><span data-stu-id="2e5e9-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="2e5e9-117">計画の最適化を開始する</span><span class="sxs-lookup"><span data-stu-id="2e5e9-117">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="2e5e9-118">計画の最適化フィット分析</span><span class="sxs-lookup"><span data-stu-id="2e5e9-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="2e5e9-119">計画の履歴と計画ログの表示</span><span class="sxs-lookup"><span data-stu-id="2e5e9-119">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="2e5e9-120">プランへのフィルターの適用</span><span class="sxs-lookup"><span data-stu-id="2e5e9-120">Apply filters to a plan</span></span>](plan-filters.md)
