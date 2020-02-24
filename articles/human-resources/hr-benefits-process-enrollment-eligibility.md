---
title: 登録の適格性を処理
description: この記事では、登録資格のプロセスを実行する方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0344c48460a7d1540481e09ba106526e119de72b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009621"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="8a133-103">登録の適格性を処理</span><span class="sxs-lookup"><span data-stu-id="8a133-103">Process enrollment eligibility</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="8a133-104">この記事では、登録資格のプロセスを実行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8a133-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="8a133-105">**給付金管理**ワークスペースにて、**処理**の下の**登録適格性の処理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a133-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="8a133-106">**給付金登録の適格性の処理を実行**ダイアログ ボックスで、次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="8a133-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="8a133-107">フィールド</span><span class="sxs-lookup"><span data-stu-id="8a133-107">Field</span></span> | <span data-ttu-id="8a133-108">説明</span><span class="sxs-lookup"><span data-stu-id="8a133-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="8a133-109">登録期間</span><span class="sxs-lookup"><span data-stu-id="8a133-109">Enrollment period</span></span> | <span data-ttu-id="8a133-110">登録適格性を処理する登録期間。</span><span class="sxs-lookup"><span data-stu-id="8a133-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="8a133-111">法人エンティティ</span><span class="sxs-lookup"><span data-stu-id="8a133-111">Legal entity</span></span> | <span data-ttu-id="8a133-112">登録適格性を処理する法人が変更されます。</span><span class="sxs-lookup"><span data-stu-id="8a133-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="8a133-113">ワーカー</span><span class="sxs-lookup"><span data-stu-id="8a133-113">Worker</span></span> | <span data-ttu-id="8a133-114">登録適格性を処理する作業者が変更されます。</span><span class="sxs-lookup"><span data-stu-id="8a133-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="8a133-115">このフィールドを空白のままにすると、登録適格性がすべての作業者に対して処理されます。</span><span class="sxs-lookup"><span data-stu-id="8a133-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="8a133-116">給付金計画</span><span class="sxs-lookup"><span data-stu-id="8a133-116">Benefit plan</span></span> | <span data-ttu-id="8a133-117">登録適格性を処理する給付金プランが変更されます。</span><span class="sxs-lookup"><span data-stu-id="8a133-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="8a133-118">バックグラウンドで処理を実行する場合は、**バックグラウンドで実行**を選択し、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="8a133-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="8a133-119">処理情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="8a133-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="8a133-120">定期的なジョブを設定するには、**再実行**を選び、繰り返しの情報を入植し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a133-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="8a133-121">ジョブ警告を設定するには、**警告**を選び、入庫する警告を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a133-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="8a133-122">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a133-122">Select **OK**.</span></span> <span data-ttu-id="8a133-123">設定したパラメータで処理が実行されます。</span><span class="sxs-lookup"><span data-stu-id="8a133-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="8a133-124">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a133-124">Select **OK**.</span></span>
