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
ms.openlocfilehash: ae1aa74c7e463cd0d8c8d740394b998030c8498f
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229996"
---
# <a name="process-life-event-changes"></a><span data-ttu-id="c6bda-103">ライフ イベントの変更を処理</span><span class="sxs-lookup"><span data-stu-id="c6bda-103">Process life event changes</span></span>

<span data-ttu-id="c6bda-104">2 つのライフ イベント変更における Microsoft Dynamics 365 Human Resourcesのライフ イベント 変更の処理:</span><span class="sxs-lookup"><span data-stu-id="c6bda-104">Process life event changes in Microsoft Dynamics 365 Human Resources for two life event changes:</span></span>

- <span data-ttu-id="c6bda-105">誕生日の変更</span><span class="sxs-lookup"><span data-stu-id="c6bda-105">Birthday changes</span></span>
- <span data-ttu-id="c6bda-106">適格性ルールにより、有効期限の変更をオーバーライドする</span><span class="sxs-lookup"><span data-stu-id="c6bda-106">Eligibility rule override expiration changes</span></span> 

1. <span data-ttu-id="c6bda-107">**給付金管理**ワークスペースにて、**処理**の下の**ライフ イベントの変更処理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c6bda-107">In the **Benefits management** workspace, under **Processing**, select **Life event change processing**.</span></span>

2. <span data-ttu-id="c6bda-108">**ライフ イベントの変更処理を実行**ダイアログ ボックスで、次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="c6bda-108">In the **Run life event change process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="c6bda-109">フィールド</span><span class="sxs-lookup"><span data-stu-id="c6bda-109">Field</span></span> | <span data-ttu-id="c6bda-110">説明</span><span class="sxs-lookup"><span data-stu-id="c6bda-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="c6bda-111">登録期間</span><span class="sxs-lookup"><span data-stu-id="c6bda-111">Enrollment period</span></span> | <span data-ttu-id="c6bda-112">ライフ イベントを処理する登録期間が変更されます。</span><span class="sxs-lookup"><span data-stu-id="c6bda-112">The enrollment period to process life event changes for.</span></span> |
   | <span data-ttu-id="c6bda-113">法人エンティティ</span><span class="sxs-lookup"><span data-stu-id="c6bda-113">Legal entity</span></span> | <span data-ttu-id="c6bda-114">ライフ イベントを処理する法人が変更されます。</span><span class="sxs-lookup"><span data-stu-id="c6bda-114">The legal entity to process life event changes for.</span></span> |

3. <span data-ttu-id="c6bda-115">バックグラウンドで処理を実行する場合は、**バックグラウンドで実行**を選択し、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="c6bda-115">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="c6bda-116">処理情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="c6bda-116">Enter information for the process.</span></span>

   2. <span data-ttu-id="c6bda-117">定期的なジョブを設定するには、**再実行**を選び、繰り返しの情報を入植し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c6bda-117">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="c6bda-118">ジョブ警告を設定するには、**警告**を選び、入庫する警告を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c6bda-118">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="c6bda-119">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c6bda-119">Select **OK**.</span></span> <span data-ttu-id="c6bda-120">設定したパラメータで処理が実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6bda-120">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="c6bda-121">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c6bda-121">Select **OK**.</span></span>
