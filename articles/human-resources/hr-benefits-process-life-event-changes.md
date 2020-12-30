---
title: ライフ イベントの変更を処理
description: ライフ イベント変更における Microsoft Dynamics 365 Human Resourcesのライフ イベント 変更の処理を行います。
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 39d1e94347809a1756fc4f66e5edc345c70eaf39
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419322"
---
# <a name="process-life-event-changes"></a><span data-ttu-id="3baaa-103">ライフ イベントの変更を処理</span><span class="sxs-lookup"><span data-stu-id="3baaa-103">Process life event changes</span></span>

<span data-ttu-id="3baaa-104">2 つのライフ イベント変更における Microsoft Dynamics 365 Human Resourcesのライフ イベント 変更の処理:</span><span class="sxs-lookup"><span data-stu-id="3baaa-104">Process life event changes in Microsoft Dynamics 365 Human Resources for two life event changes:</span></span>

- <span data-ttu-id="3baaa-105">誕生日の変更</span><span class="sxs-lookup"><span data-stu-id="3baaa-105">Birthday changes</span></span>
- <span data-ttu-id="3baaa-106">適格性ルールにより、有効期限の変更をオーバーライドする</span><span class="sxs-lookup"><span data-stu-id="3baaa-106">Eligibility rule override expiration changes</span></span> 

1. <span data-ttu-id="3baaa-107">**給付金管理** ワークスペースにて、**処理** の下の **ライフ イベントの変更処理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3baaa-107">In the **Benefits management** workspace, under **Processing**, select **Life event change processing**.</span></span>

2. <span data-ttu-id="3baaa-108">**ライフ イベントの変更処理を実行** ダイアログ ボックスで、次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="3baaa-108">In the **Run life event change process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="3baaa-109">フィールド</span><span class="sxs-lookup"><span data-stu-id="3baaa-109">Field</span></span> | <span data-ttu-id="3baaa-110">説明</span><span class="sxs-lookup"><span data-stu-id="3baaa-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="3baaa-111">登録期間</span><span class="sxs-lookup"><span data-stu-id="3baaa-111">Enrollment period</span></span> | <span data-ttu-id="3baaa-112">ライフ イベントを処理する登録期間が変更されます。</span><span class="sxs-lookup"><span data-stu-id="3baaa-112">The enrollment period to process life event changes for.</span></span> |
   | <span data-ttu-id="3baaa-113">法人エンティティ</span><span class="sxs-lookup"><span data-stu-id="3baaa-113">Legal entity</span></span> | <span data-ttu-id="3baaa-114">ライフ イベントを処理する法人が変更されます。</span><span class="sxs-lookup"><span data-stu-id="3baaa-114">The legal entity to process life event changes for.</span></span> |

3. <span data-ttu-id="3baaa-115">バックグラウンドで処理を実行する場合は、**バックグラウンドで実行** を選択し、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="3baaa-115">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="3baaa-116">処理情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="3baaa-116">Enter information for the process.</span></span>

   2. <span data-ttu-id="3baaa-117">定期的なジョブを設定するには、**再実行** を選び、繰り返しの情報を入植し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3baaa-117">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="3baaa-118">ジョブ警告を設定するには、**警告** を選び、入庫する警告を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3baaa-118">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="3baaa-119">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3baaa-119">Select **OK**.</span></span> <span data-ttu-id="3baaa-120">設定したパラメータで処理が実行されます。</span><span class="sxs-lookup"><span data-stu-id="3baaa-120">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="3baaa-121">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3baaa-121">Select **OK**.</span></span>
