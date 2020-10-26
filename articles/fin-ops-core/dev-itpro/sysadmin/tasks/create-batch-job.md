---
title: バッチ ジョブの作成
description: バッチ ジョブは、自動処理のために Application Object Server (AOS) インスタンスに送信されるタスクのグループです。
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4903724adc9deaa40b6cd04c215273dd4b0522d4
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982529"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="bc5ed-103">バッチ ジョブの作成</span><span class="sxs-lookup"><span data-stu-id="bc5ed-103">Create a batch job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bc5ed-104">バッチ ジョブは、自動処理のために Application Object Server (AOS) インスタンスに送信されるタスクのグループです。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="bc5ed-105">バッチ ジョブは、ジョブを作成したユーザーのセキュリティ資格情報を使用して実行されます。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="bc5ed-106">バッチ ジョブを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="bc5ed-107">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="bc5ed-108">バッチ ジョブの作成</span><span class="sxs-lookup"><span data-stu-id="bc5ed-108">Create the batch job</span></span>
1. <span data-ttu-id="bc5ed-109">**ナビゲーション ウィンドウ > モジュール > システム管理 > 紹介 > バッチ ジョブ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-109">Go to **Navigation pane > Modules > System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="bc5ed-110">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-110">Click **New**.</span></span>
3. <span data-ttu-id="bc5ed-111">**ジョブの説明**フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-111">In the **Job description** field, type a value.</span></span>
4. <span data-ttu-id="bc5ed-112">**開始予定日時**フィールドに、日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-112">In the **Scheduled start date/time** field, enter a date and time.</span></span>
5. <span data-ttu-id="bc5ed-113">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-113">Click **Save**.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="bc5ed-114">再実行の作成</span><span class="sxs-lookup"><span data-stu-id="bc5ed-114">Create a recurrence</span></span>
1. <span data-ttu-id="bc5ed-115">アクションウィンドウで、**バッチ ジョブ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-115">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="bc5ed-116">**再実行**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-116">Click **Recurrence**.</span></span> <span data-ttu-id="bc5ed-117">これらのオプションを使用して再実行の範囲とパターンを入力します。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="bc5ed-118">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-118">Click **OK**.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="bc5ed-119">警告の追加</span><span class="sxs-lookup"><span data-stu-id="bc5ed-119">Add alerts</span></span>
1. <span data-ttu-id="bc5ed-120">アクションウィンドウで、**バッチ ジョブ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-120">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="bc5ed-121">**警告**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-121">Click **Alerts**.</span></span> <span data-ttu-id="bc5ed-122">バッチ ジョブの終了時、エラー発生時、またはキャンセル時に警告メッセージを表示するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="bc5ed-123">そして、警告をポップアップ メッセージとして表示するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="bc5ed-124">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-124">Click **OK**.</span></span>

## <a name="adjust-batch-job-status"></a><span data-ttu-id="bc5ed-125">バッチ ジョブ状態の調整</span><span class="sxs-lookup"><span data-stu-id="bc5ed-125">Adjust batch job status</span></span>
1. <span data-ttu-id="bc5ed-126">**システム管理 > 照会 > バッチ ジョブ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-126">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="bc5ed-127">適切なバッチ ジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-127">Select the appropriate batch job.</span></span>
3. <span data-ttu-id="bc5ed-128">アクション ウィンドウで、**バッチ ジョブ > 機能 > 状態の変更**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-128">On the Action Pane, click **Batch job > Functions > Change status**.</span></span>
4. <span data-ttu-id="bc5ed-129">適切な状態を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-129">Select the appropriate status:</span></span>
    - <span data-ttu-id="bc5ed-130">**源泉徴収** : バッチ ジョブを**源泉徴収**に設定して、バッチ ジョブ スケジューラから源泉徴収されるようにします。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-130">**Withhold**: Set the batch job as **withhold** so it is withheld from the batch job scheduler.</span></span> <span data-ttu-id="bc5ed-131">*停止*することを意味します。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-131">Equivalent to *stop*.</span></span>
    - <span data-ttu-id="bc5ed-132">**待機中** : バッチ ジョブを**待機中**に設定して、バッチ ジョブ スケジューラによる集荷を待機します。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-132">**Waiting**: Set the batch job as **waiting** so it is waiting to be picked up by the batch job scheduler.</span></span> <span data-ttu-id="bc5ed-133">*移動*することを意味します。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-133">Equivalent to *go*.</span></span>
5. <span data-ttu-id="bc5ed-134">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5ed-134">Click **OK**.</span></span>
