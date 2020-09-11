---
title: ライフ イベントの適格性を処理
description: この記事では、ライフ イベント適格性の処理を実行する方法について説明します。
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
ms.openlocfilehash: 17ecef1412eb0232fbb4782bd9d2d79f210c7e80
ms.sourcegitcommit: 9723b5ff40c84677316d71e185cf862556b32cf9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/31/2020
ms.locfileid: "3741390"
---
# <a name="process-life-event-eligibility"></a><span data-ttu-id="f5f60-103">ライフ イベントの適格性を処理</span><span class="sxs-lookup"><span data-stu-id="f5f60-103">Process life event eligibility</span></span>

<span data-ttu-id="f5f60-104">この記事では、ライフ イベント適格性の処理を実行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f5f60-104">This article shows you how to run the process for life event eligibility.</span></span>

1. <span data-ttu-id="f5f60-105">**給付金管理**ワークスペースにて、**処理**の下の**ライフ イベントの適格性処理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f5f60-105">In the **Benefits management** workspace, under **Processing**, select **Life event eligibility processing**.</span></span>

2. <span data-ttu-id="f5f60-106">**ライフ イベントの適格性処理を実行**ダイアログ ボックスで、次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="f5f60-106">In the **Run life event eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="f5f60-107">フィールド</span><span class="sxs-lookup"><span data-stu-id="f5f60-107">Field</span></span> | <span data-ttu-id="f5f60-108">説明</span><span class="sxs-lookup"><span data-stu-id="f5f60-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f5f60-109">**登録期間**</span><span class="sxs-lookup"><span data-stu-id="f5f60-109">**Enrollment period**</span></span> | <span data-ttu-id="f5f60-110">ライフ イベントの適格性を処理する登録期間。</span><span class="sxs-lookup"><span data-stu-id="f5f60-110">The enrollment period to process life event eligibility for.</span></span> |

3. <span data-ttu-id="f5f60-111">バックグラウンドで処理を実行する場合は、**バックグラウンドで実行**を選択し、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="f5f60-111">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="f5f60-112">処理情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="f5f60-112">Enter information for the process.</span></span>

   2. <span data-ttu-id="f5f60-113">定期的なジョブを設定するには、**再実行**を選び、繰り返しの情報を入植し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f5f60-113">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="f5f60-114">ジョブ警告を設定するには、**警告**を選び、入庫する警告を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f5f60-114">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="f5f60-115">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f5f60-115">Select **OK**.</span></span> <span data-ttu-id="f5f60-116">設定したパラメータで処理が実行されます。</span><span class="sxs-lookup"><span data-stu-id="f5f60-116">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="f5f60-117">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f5f60-117">Select **OK**.</span></span>
