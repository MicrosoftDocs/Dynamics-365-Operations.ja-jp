---
title: Dynamics 365 Talent の新機能および変更された機能 (2019 年 2 月 7 日)
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2019
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
ms.author: dkrame
ms.search.validFrom: 2019-02-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 002dcd8253a0ab753ac9002e7027441db6d0b858
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461777"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-7-2019"></a><span data-ttu-id="18664-103">Dynamics 365 Talent の新機能および変更された機能 (2019 年 2 月 7 日)</span><span class="sxs-lookup"><span data-stu-id="18664-103">What's new or changed in Dynamics 365 Talent (February 7, 2019)</span></span>

<span data-ttu-id="18664-104">このトピックでは、 Talent の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="18664-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="18664-105">Attract の変更</span><span class="sxs-lookup"><span data-stu-id="18664-105">Changes in Attract</span></span>

### <a name="interview-scheduling-enhancements"></a><span data-ttu-id="18664-106">面接のスケジューリングの拡張</span><span class="sxs-lookup"><span data-stu-id="18664-106">Interview scheduling enhancements</span></span>
<span data-ttu-id="18664-107">エンド ツー エンドの面接のスケジューリング エクスペリエンスに改良が加えられました。</span><span class="sxs-lookup"><span data-stu-id="18664-107">Improvements have been made to the end-to-end interview scheduling experience.</span></span> <span data-ttu-id="18664-108">これで、内部候補者のカレンダーの空き状況を確認したり、スケジュールの推奨事項に内部候補者のカレンダーを使用したりできます。</span><span class="sxs-lookup"><span data-stu-id="18664-108">You can now see the calendar availability of an internal candidate and use the internal candidate’s calendar for schedule recommendations.</span></span> <span data-ttu-id="18664-109">詳細については、[面接のスケジューリングおよびフィードバック](interview-scheduling-feedback.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="18664-109">For more information, see [Interview scheduling and feedback](interview-scheduling-feedback.md).</span></span>

### <a name="job-posting-to-linkedin--company-mismatch-issue-fixed"></a><span data-ttu-id="18664-110">LinkedIn へのジョブ求人転記 – 会社が一致しない問題の修正</span><span class="sxs-lookup"><span data-stu-id="18664-110">Job posting to LinkedIn – company mismatch issue fixed</span></span>
<span data-ttu-id="18664-111">Attract から LinkedIn に転記されたジョブ求人が間違った会社名で表示される問題が修正されています。</span><span class="sxs-lookup"><span data-stu-id="18664-111">An issue has been fixed where jobs posted to LinkedIn from Attract were appearing under the wrong company name.</span></span> <span data-ttu-id="18664-112">詳細については、[Attract でのジョブの作成、承認、および転記](creating-jobs-attract.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="18664-112">For more information, see [Create, approve, and post jobs in Attract](creating-jobs-attract.md).</span></span>

### <a name="career-site-url-displayed-in-admin-settings"></a><span data-ttu-id="18664-113">管理者の設定に表示されるキャリア サイトの URL</span><span class="sxs-lookup"><span data-stu-id="18664-113">Career site URL displayed in Admin settings</span></span>
<span data-ttu-id="18664-114">**キャリア サイトの管理** の **管理者設定** にキャリア サイトのホーム ページの URL が表示されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="18664-114">The career site home page URL is now displayed in **Admin Settings** under **Career Site management**.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="18664-115">Core HR の変更</span><span class="sxs-lookup"><span data-stu-id="18664-115">Changes in Core HR</span></span>

<span data-ttu-id="18664-116">**ビルド 8.1.2134**</span><span class="sxs-lookup"><span data-stu-id="18664-116">**Build 8.1.2134**</span></span>

### <a name="multiple-compensation-levels-supported-on-jobs"></a><span data-ttu-id="18664-117">ジョブでサポートされている複数の報酬レベル</span><span class="sxs-lookup"><span data-stu-id="18664-117">Multiple compensation levels supported on jobs</span></span>
<span data-ttu-id="18664-118">この変更により、1 つのジョブに複数の報酬レベルを定義することが可能になり、同じジョブを使用する場合にプラン間で異なる従業員の固定報酬範囲が可能になります。</span><span class="sxs-lookup"><span data-stu-id="18664-118">This change allows for more than one compensation level to be defined on a job, enabling employee fixed compensation ranges which may differ between plans when using the same job.</span></span> 

<span data-ttu-id="18664-119">例:</span><span class="sxs-lookup"><span data-stu-id="18664-119">For example:</span></span>    
<span data-ttu-id="18664-120">*ジョブ* - アカウント マネージャー *関連付けられている報酬レベル:* B1 および B2 - 各レベルには、定義された値の範囲があります。</span><span class="sxs-lookup"><span data-stu-id="18664-120">*Job* - Account Manager *Associated compensation levels:* B1 and B2 - Each level has a defined range of values.</span></span> <span data-ttu-id="18664-121">B1 = 最小 50,000、平均 60,000、最大 75,000 および B2 = 最小 65,000、平均 74,000、最大 85,000。</span><span class="sxs-lookup"><span data-stu-id="18664-121">B1 = Min 50,000, Mid 60,000, Max 75,000 and B2 = Min 65,000, Mid 74,000, Max 85,000.</span></span> <span data-ttu-id="18664-122">定義された適格性ルールに基づいて従業員に固定報酬を作成するときに、各固定プランは同じジョブとそのジョブの異なるレベルを指すようになりました。</span><span class="sxs-lookup"><span data-stu-id="18664-122">When creating fixed compensation for employees, based on the eligibility rules defined, each fixed plan can now point to the same job and to different levels on the job.</span></span> <span data-ttu-id="18664-123">これにより、異なる地域/会社でプランを定義し、これらの違いを説明するためにジョブを重複させることなく、同じジョブで異なる範囲を指すようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="18664-123">This allows for plans to be defined in different regions/companies and point to the same job but different ranges without duplicating jobs to account for these differences.</span></span>

### <a name="compensation-level-field-has-been-added-to-the-employee-fixed-compensation-entity"></a><span data-ttu-id="18664-124">報酬レベル フィールドを従業員の固定報酬エンティティに追加</span><span class="sxs-lookup"><span data-stu-id="18664-124">Compensation level field has been added to the Employee fixed compensation entity</span></span> 
<span data-ttu-id="18664-125">この更新により、従業員の固定報酬のエンティティは **報酬レベル** フィールドを含むようになりました。</span><span class="sxs-lookup"><span data-stu-id="18664-125">With this update, the employee fixed compensation entity has been updated to include the **Compensation level** field.</span></span> <span data-ttu-id="18664-126">この追加によって、従業員の固定報酬プランの更新が簡単になりました。</span><span class="sxs-lookup"><span data-stu-id="18664-126">This addition makes it easier to update employee fixed compensation plans.</span></span> 

### <a name="update-job-family-when-updating-and-creating-new-positions"></a><span data-ttu-id="18664-127">新しい職位を更新および作成するときにジョブのファミリを更新する</span><span class="sxs-lookup"><span data-stu-id="18664-127">Update Job family when updating and creating new positions</span></span>
<span data-ttu-id="18664-128">職位のジョブを変更すると、**ジョブのファミリ** が選択されているジョブに基づいて既定として設定されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="18664-128">When changing the job on a position, **Job family** will now default based on the job selected.</span></span>

### <a name="performance-improvements-when-rendering-workspaces"></a><span data-ttu-id="18664-129">ワークスペースをレンダリングするときのパフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="18664-129">Performance improvements when rendering workspaces</span></span>
<span data-ttu-id="18664-130">ワークスペースの分析タブはそれらのページにアクセスしたときにのみ読み込まれるようになりました。</span><span class="sxs-lookup"><span data-stu-id="18664-130">Analytics tabs on workspaces will now load only when accessing those pages.</span></span> <span data-ttu-id="18664-131">ページの最初のレンダリングの際に、ページの左上隅にインジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="18664-131">An indicator will display during the initial rendering of the page in the upper-left corner of the page.</span></span>
