---
title: Dynamics 365 Talent の新機能および変更された機能 (2019 年 1 月 31 日)
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 01/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8e8c11e460a4678efea81f8d3d1eec96b673d329
ms.sourcegitcommit: 53174ed4e7cc4e1ba07cdfc39207e7296ef87c1f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/07/2020
ms.locfileid: "4690055"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-31-2019"></a><span data-ttu-id="e0a21-103">Dynamics 365 Talent の新機能および変更された機能 (2019 年 1 月 31 日)</span><span class="sxs-lookup"><span data-stu-id="e0a21-103">What's new or changed in Dynamics 365 Talent (January 31, 2019)</span></span>

<span data-ttu-id="e0a21-104">このトピックでは、Dynamics 365 Talent の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="e0a21-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

<span data-ttu-id="e0a21-105">**ビルド 8.1.2128**</span><span class="sxs-lookup"><span data-stu-id="e0a21-105">**Build 8.1.2128**</span></span>

## <a name="core-hr-changes"></a><span data-ttu-id="e0a21-106">Core HR の変更</span><span class="sxs-lookup"><span data-stu-id="e0a21-106">Core HR Changes</span></span>

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a><span data-ttu-id="e0a21-107">休暇人員カード上で実行された休暇には休暇の計画日は考慮されません</span><span class="sxs-lookup"><span data-stu-id="e0a21-107">Time off taken on leave people card doesn't consider leave plan dates</span></span>
<span data-ttu-id="e0a21-108">暦年に実行されない休暇プランの場合、**取得** カードがプランで定義された休暇年に取得された休暇を表示するようになりました。</span><span class="sxs-lookup"><span data-stu-id="e0a21-108">For leave plans that don’t run on a calendar year, the **Taken** card now displays time off that’s been taken in the plan-defined leave year.</span></span> <span data-ttu-id="e0a21-109">たとえば、組織の休暇年が 6 月 1 日から 5 月 30 日で、ある従業員が 12 月に 3 日間休みを取った場合、1 月 15 日の **取得** カードには 3 日間が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0a21-109">For example, if an organization’s leave year is June 1 through May 30 and an employee has taken three days off in December, the **Taken** card on January 15, will display 3 days.</span></span> 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a><span data-ttu-id="e0a21-110">見越計上金額が層日付基準と一致しません</span><span class="sxs-lookup"><span data-stu-id="e0a21-110">Accrual amounts not matching tier date basis</span></span>
<span data-ttu-id="e0a21-111">顧客が従業員のどのサービス日付が有効なのかを判断できるようにするために、休暇および欠勤 (**人事管理** パラメーター) に新しいオプションが追加されました。</span><span class="sxs-lookup"><span data-stu-id="e0a21-111">New options have been added to leave and absence (**Human resources** parameters) to enable customers to determine when employees’ months of service date are effective.</span></span> <span data-ttu-id="e0a21-112">一部の組織では日付は月末ですが、他の組織では翌月の初めになる場合があります。</span><span class="sxs-lookup"><span data-stu-id="e0a21-112">For some organizations, the date is the end of the month, but for others it may be the start of the next month.</span></span> <span data-ttu-id="e0a21-113">たとえば、ある組織が 12 月 31 日に休暇を与え、別の組織は 1 月 1 日に休暇を与える場合があります。</span><span class="sxs-lookup"><span data-stu-id="e0a21-113">For example, one organization may award time off on December 31, while another may award time off on January 1.</span></span> <span data-ttu-id="e0a21-114">このオプションでは、報酬を発行する時を選択できます。</span><span class="sxs-lookup"><span data-stu-id="e0a21-114">This option will allow you to choose when the award should occur.</span></span> 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a><span data-ttu-id="e0a21-115">作業者の採用アクションが「ワークフロー完了」の状態で止まっています</span><span class="sxs-lookup"><span data-stu-id="e0a21-115">Worker hire actions are stuck in "Workflow complete" state</span></span>
<span data-ttu-id="e0a21-116">いくつかのワークフローが「ワークフロー完了」の状態で終了する問題を修正するための変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="e0a21-116">Changes have been made to correct an issue where a small number of workflows finished with a "Workflow complete" status.</span></span> <span data-ttu-id="e0a21-117">ワークフローが終了すると、新しいワークフローは「完了」の状態に移行するようになりました。</span><span class="sxs-lookup"><span data-stu-id="e0a21-117">New workflows should now move to a "Completed" state when the workflow finishes.</span></span> <span data-ttu-id="e0a21-118">ワークフロー完了状態のワークフローはすべてエラー ステータスに移行され、必要に応じて更新または削除が可能になります。</span><span class="sxs-lookup"><span data-stu-id="e0a21-118">Any workflows in a workflow completed status will be transitioned to an error status to allow for updating or removal if required.</span></span> 
