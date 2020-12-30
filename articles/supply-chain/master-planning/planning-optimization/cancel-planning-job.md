---
title: 計画ジョブのキャンセル
description: このトピックでは、計画の最適化機能を使用する有効な計画ジョブを取り消す方法について説明します。
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4b65d344cd764740cc1485969c2fc4c2052e55e2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431935"
---
# <a name="cancel-a-planning-job"></a><span data-ttu-id="eb0d5-103">計画ジョブのキャンセル</span><span class="sxs-lookup"><span data-stu-id="eb0d5-103">Cancel a planning job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eb0d5-104">Microsoft Dynamics 365 Supply Chain Management では、計画の最適化機能を使用する有効な計画ジョブを取り消す方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="eb0d5-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning optimization functionality.</span></span> <span data-ttu-id="eb0d5-105">計画最適化ジョブがユーザー インターフェイス (バックグラウンドではなく) から直接トリガーされた際、ダイアログ ボックスで **キャンセル** を選択すると、計画最適化ジョブはキャンセルされません。</span><span class="sxs-lookup"><span data-stu-id="eb0d5-105">When you select **Cancel** in the dialog box when a Planning optimization job is triggered directly from the user interface (not in the background), this will not cancel the Planning optimization job.</span></span> <span data-ttu-id="eb0d5-106">「処理が取り消されました」などの警告が表示された場合でも、計画最適化で計画ジョブをキャンセルするには、次の手順を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb0d5-106">Even if you receive a warning such as “Operation canceled”, you will still need to use the following steps to cancel a planning job with Planning optimization.</span></span>


<span data-ttu-id="eb0d5-107">有効な計画ジョブをキャンセルするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="eb0d5-107">To cancel an active planning job, follow these steps.</span></span> 

> [!NOTE]
> <span data-ttu-id="eb0d5-108">有効なジョブのみキャンセルすることができます。</span><span class="sxs-lookup"><span data-stu-id="eb0d5-108">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="eb0d5-109">**マスタープラン \> 設定 \> 計画** に移動します。</span><span class="sxs-lookup"><span data-stu-id="eb0d5-109">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="eb0d5-110">計画実行に適切な計画を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb0d5-110">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="eb0d5-111">**履歴** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb0d5-111">Select **History**.</span></span>
4. <span data-ttu-id="eb0d5-112">キャンセルする計画ジョブの選択</span><span class="sxs-lookup"><span data-stu-id="eb0d5-112">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="eb0d5-113">**キャンセル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb0d5-113">Select **Cancel**.</span></span>

<span data-ttu-id="eb0d5-114">ジョブ状態は、計画の最適化サービスがジョブのキャンセルを確認するまで **キャンセル中** になります。</span><span class="sxs-lookup"><span data-stu-id="eb0d5-114">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="eb0d5-115">その後、状態は **キャンセル済** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="eb0d5-115">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="eb0d5-116">状態の変更を確認するには、**更新** ボタンを選択してページを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb0d5-116">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eb0d5-117">追加リソース</span><span class="sxs-lookup"><span data-stu-id="eb0d5-117">Additional resources</span></span>

[<span data-ttu-id="eb0d5-118">計画最適化の概要</span><span class="sxs-lookup"><span data-stu-id="eb0d5-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="eb0d5-119">計画最適化の開始</span><span class="sxs-lookup"><span data-stu-id="eb0d5-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="eb0d5-120">計画の最適化フィット分析</span><span class="sxs-lookup"><span data-stu-id="eb0d5-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="eb0d5-121">計画の履歴と計画ログの表示</span><span class="sxs-lookup"><span data-stu-id="eb0d5-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="eb0d5-122">プランへのフィルターの適用</span><span class="sxs-lookup"><span data-stu-id="eb0d5-122">Apply filters to a plan</span></span>](plan-filters.md)
