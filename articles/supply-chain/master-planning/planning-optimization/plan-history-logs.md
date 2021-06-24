---
title: 計画の履歴と計画ログの表示
description: このトピックでは、計画の最適化機能によってトリガーされる計画ジョブの履歴を表示する方法について説明します。
author: ChristianRytt
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: d7bba084b03f8698c8bf31d171d5e4e486ed06ad
ms.sourcegitcommit: a7649b361ec54b49c0e9ee1c1c63a8815f320225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187250"
---
# <a name="view-plan-history-and-planning-logs"></a><span data-ttu-id="59686-103">計画の履歴と計画ログの表示</span><span class="sxs-lookup"><span data-stu-id="59686-103">View plan history and planning logs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="59686-104">このトピックでは、Microsoft Dynamics 365 Supply Chain Management で計画の最適化機能によってトリガーされる計画ジョブの履歴を表示する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="59686-104">This topic explains how to view the history of planning jobs that are triggered by the Planning Optimization functionality in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="59686-105">計画の履歴を表示するには、**マスター プラン** \> **設定** \> **計画** \> **マスター プラン** の順に移動して **履歴** を選択することにより、計画を開きます。</span><span class="sxs-lookup"><span data-stu-id="59686-105">To view the history for a plan, open the plan by going to **Master planning** \> **Setup** \> **Plans** \> **Master plans** and selecting **History**.</span></span> <span data-ttu-id="59686-106">履歴には、選択された計画のすべてのジョブが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="59686-106">The history lists all the jobs for the selected plan.</span></span> <span data-ttu-id="59686-107">一覧には、完了ジョブおよび有効なジョブが含まれます。</span><span class="sxs-lookup"><span data-stu-id="59686-107">The list includes completed and active jobs.</span></span>

<span data-ttu-id="59686-108">計画の最適化マスター プラン実行のジョブ履歴は、マスター プランごとに最大 60 件のレコードまで保持されます。</span><span class="sxs-lookup"><span data-stu-id="59686-108">The history of jobs for Planning Optimization master planning runs keeps only up to 60 records per master plan.</span></span> <span data-ttu-id="59686-109">新しいマスター プラン計算を実行するたびに、その計画の最も早い履歴レコードが削除されます。</span><span class="sxs-lookup"><span data-stu-id="59686-109">Whenever you run a new master planning calculation, that plan's earliest history record is deleted.</span></span>

<span data-ttu-id="59686-110">ジョブの開始時刻とステータスが表示されるのに加えて、特定のジョブのログも表示できます。</span><span class="sxs-lookup"><span data-stu-id="59686-110">In addition to seeing the start time and status of jobs, you can view the log for a specific job.</span></span> <span data-ttu-id="59686-111">ログには、追加の情報および警告が含まれます。</span><span class="sxs-lookup"><span data-stu-id="59686-111">The log includes additional information and warnings.</span></span> <span data-ttu-id="59686-112">すべてのジョブにログがあるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="59686-112">Not all jobs have a log.</span></span> <span data-ttu-id="59686-113">ジョブのログを表示するには、**ログ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59686-113">To view the log for a job, select **Log**.</span></span> <span data-ttu-id="59686-114">ログ エントリは、ジョブが完了した日から 30 日間のみ、自動的に削除された後に保存されます。</span><span class="sxs-lookup"><span data-stu-id="59686-114">Log entries are only stored for 30 days after the date the job finished, after that they are automatically deleted.</span></span>

## <a name="related-resources"></a><span data-ttu-id="59686-115">関連するリソース</span><span class="sxs-lookup"><span data-stu-id="59686-115">Related resources</span></span>

- [<span data-ttu-id="59686-116">計画最適化の概要</span><span class="sxs-lookup"><span data-stu-id="59686-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)
- [<span data-ttu-id="59686-117">計画最適化の開始</span><span class="sxs-lookup"><span data-stu-id="59686-117">Get started with Planning Optimization</span></span>](get-started.md)
- [<span data-ttu-id="59686-118">計画の最適化フィット分析</span><span class="sxs-lookup"><span data-stu-id="59686-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)
- [<span data-ttu-id="59686-119">プランへのフィルターの適用</span><span class="sxs-lookup"><span data-stu-id="59686-119">Apply filters to a plan</span></span>](plan-filters.md)
- [<span data-ttu-id="59686-120">計画ジョブのキャンセル</span><span class="sxs-lookup"><span data-stu-id="59686-120">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]