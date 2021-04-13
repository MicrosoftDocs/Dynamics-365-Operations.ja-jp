---
title: バッチ ビジネス イベント
description: このトピックでは、バッチ ビジネス イベントの詳細情報を提供します。
author: sarvanisathish
ms.date: 02/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2021-03-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 573941023fcd5e4f6f59b0275d0f0d71f10de1c2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745349"
---
# <a name="batch-business-events"></a><span data-ttu-id="2913c-103">バッチ ビジネス イベント</span><span class="sxs-lookup"><span data-stu-id="2913c-103">Batch business events</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2913c-104">バッチ フレームワークは、次のシステム ビジネス イベントを出力します。</span><span class="sxs-lookup"><span data-stu-id="2913c-104">The batch framework emits the following system business events.</span></span>

| <span data-ttu-id="2913c-105">ビジネス イベント</span><span class="sxs-lookup"><span data-stu-id="2913c-105">Business event</span></span> | <span data-ttu-id="2913c-106">説明</span><span class="sxs-lookup"><span data-stu-id="2913c-106">Description</span></span> | <span data-ttu-id="2913c-107">モジュール</span><span class="sxs-lookup"><span data-stu-id="2913c-107">Module</span></span> |
|----------------|-------------|--------|
| <span data-ttu-id="2913c-108">バッチ ジョブの開始</span><span class="sxs-lookup"><span data-stu-id="2913c-108">Batch job started</span></span> | <span data-ttu-id="2913c-109">このイベントは、バッチ ジョブが実行中としてマークされているときに発生します。</span><span class="sxs-lookup"><span data-stu-id="2913c-109">This event is fired when a batch job is marked as running.</span></span> | <span data-ttu-id="2913c-110">バッチ</span><span class="sxs-lookup"><span data-stu-id="2913c-110">Batch</span></span> |
| <span data-ttu-id="2913c-111">バッチ ジョブの終了</span><span class="sxs-lookup"><span data-stu-id="2913c-111">Batch job finished</span></span> | <span data-ttu-id="2913c-112">このイベントは、バッチ ジョブが完了としてマークされているときに発生します。</span><span class="sxs-lookup"><span data-stu-id="2913c-112">This event is fired when a batch job is completed.</span></span> | <span data-ttu-id="2913c-113">バッチ</span><span class="sxs-lookup"><span data-stu-id="2913c-113">Batch</span></span> |
| <span data-ttu-id="2913c-114">バッチ ジョブの失敗</span><span class="sxs-lookup"><span data-stu-id="2913c-114">Batch job failed</span></span> | <span data-ttu-id="2913c-115">このイベントは、バッチ ジョブが失敗としてマークされているときに発生します。</span><span class="sxs-lookup"><span data-stu-id="2913c-115">This event is fired when a batch job fails.</span></span> | <span data-ttu-id="2913c-116">バッチ</span><span class="sxs-lookup"><span data-stu-id="2913c-116">Batch</span></span> |
| <span data-ttu-id="2913c-117">バッチ ジョブのキャンセル</span><span class="sxs-lookup"><span data-stu-id="2913c-117">Batch job cancelled</span></span> | <span data-ttu-id="2913c-118">このイベントは、バッチ ジョブがキャンセルとしてマークされているときに発生します。</span><span class="sxs-lookup"><span data-stu-id="2913c-118">This event is fired when a batch job is canceled.</span></span> | <span data-ttu-id="2913c-119">バッチ</span><span class="sxs-lookup"><span data-stu-id="2913c-119">Batch</span></span> |

## <a name="usage"></a><span data-ttu-id="2913c-120">用途</span><span class="sxs-lookup"><span data-stu-id="2913c-120">Usage</span></span>

### <a name="batch-job-started-and-batch-job-finished"></a><span data-ttu-id="2913c-121">バッチ ジョブの開始およびバッチ ジョブの完了</span><span class="sxs-lookup"><span data-stu-id="2913c-121">Batch job started and batch job finished</span></span>

<span data-ttu-id="2913c-122">**バッチ ジョブの開始** および **バッチ ジョブの完了** イベントは、実行時間の長いバッチ ジョブの監視および特定を行うために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2913c-122">The **batch job started** and **batch job finished** events can be used to monitor and identify long-running batch jobs.</span></span> <span data-ttu-id="2913c-123">ジョブに予想以上の時間がかかる場合に関係者に通知するためにも使用できます。</span><span class="sxs-lookup"><span data-stu-id="2913c-123">They can also be used to notify stakeholders if a job takes longer than expected.</span></span> <span data-ttu-id="2913c-124">既定では、これらのイベントはアプリケーションで無効になっています。</span><span class="sxs-lookup"><span data-stu-id="2913c-124">By default, these events are turned off in the application.</span></span>

### <a name="batch-job-failed"></a><span data-ttu-id="2913c-125">バッチ ジョブの失敗</span><span class="sxs-lookup"><span data-stu-id="2913c-125">Batch job failed</span></span>

<span data-ttu-id="2913c-126">**バッチ ジョブの失敗** イベントは、特定のバッチ ジョブが失敗していないか監視し、リアルタイムに関係者に通知するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="2913c-126">The **batch job failed** event can be used to monitor specific batch jobs for failure, and to notify stakeholders in real time.</span></span> <span data-ttu-id="2913c-127">既定では、このイベントはアプリケーションで有効になっています。</span><span class="sxs-lookup"><span data-stu-id="2913c-127">By default, this event is turned on in the application.</span></span>

## <a name="configure-batch-business-events"></a><span data-ttu-id="2913c-128">バッチ ビジネス イベントのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="2913c-128">Configure batch business events</span></span>

1. <span data-ttu-id="2913c-129">**システム管理 \> 照会 \> バッチ ジョブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2913c-129">Go to **System administration \> Inquiries \> Batch jobs**.</span></span>
2. <span data-ttu-id="2913c-130">**ビジネス イベント** タブで設定を更新して、バッチ ビジネス イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="2913c-130">On the **Business events** tab, update the settings to raise batch business events.</span></span>

<span data-ttu-id="2913c-131">イベントには次のペイロードが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2913c-131">The events have the following payload.</span></span>

| <span data-ttu-id="2913c-132">フィールド名</span><span class="sxs-lookup"><span data-stu-id="2913c-132">Field name</span></span> | <span data-ttu-id="2913c-133">フィールド ラベル</span><span class="sxs-lookup"><span data-stu-id="2913c-133">Field label</span></span> |
|------------|-------------|
| <span data-ttu-id="2913c-134">JobId</span><span class="sxs-lookup"><span data-stu-id="2913c-134">JobId</span></span> | <span data-ttu-id="2913c-135">バッチ ジョブ ID</span><span class="sxs-lookup"><span data-stu-id="2913c-135">Batch job ID</span></span> |
| <span data-ttu-id="2913c-136">JobDescription</span><span class="sxs-lookup"><span data-stu-id="2913c-136">JobDescription</span></span> | <span data-ttu-id="2913c-137">バッチ ジョブの説明</span><span class="sxs-lookup"><span data-stu-id="2913c-137">Batch job description</span></span> |
| <span data-ttu-id="2913c-138">JobStatus</span><span class="sxs-lookup"><span data-stu-id="2913c-138">JobStatus</span></span> | <span data-ttu-id="2913c-139">バッチ ジョブの状態</span><span class="sxs-lookup"><span data-stu-id="2913c-139">Batch job status</span></span> |
| <span data-ttu-id="2913c-140">JobOwnerEmailId</span><span class="sxs-lookup"><span data-stu-id="2913c-140">JobOwnerEmailId</span></span> | <span data-ttu-id="2913c-141">バッチ ジョブの所有者の電子メール ID</span><span class="sxs-lookup"><span data-stu-id="2913c-141">Batch job owner email ID</span></span> |
| <span data-ttu-id="2913c-142">JobExecutedByEmailId</span><span class="sxs-lookup"><span data-stu-id="2913c-142">JobExecutedByEmailId</span></span> | <span data-ttu-id="2913c-143">電子メール ID によって実行されたバッチ ジョブ</span><span class="sxs-lookup"><span data-stu-id="2913c-143">Batch job executed by email ID</span></span> |
| <span data-ttu-id="2913c-144">AdminEmailId</span><span class="sxs-lookup"><span data-stu-id="2913c-144">AdminEmailId</span></span> | <span data-ttu-id="2913c-145">管理者ユーザーの電子メール ID</span><span class="sxs-lookup"><span data-stu-id="2913c-145">Admin user email ID</span></span> |
| <span data-ttu-id="2913c-146">JobEndUtcDateTime</span><span class="sxs-lookup"><span data-stu-id="2913c-146">JobEndUtcDateTime</span></span> | <span data-ttu-id="2913c-147">ジョブ終了の UTC 日時</span><span class="sxs-lookup"><span data-stu-id="2913c-147">Job end UTC date time</span></span> |
| <span data-ttu-id="2913c-148">BusinessEventId</span><span class="sxs-lookup"><span data-stu-id="2913c-148">BusinessEventId</span></span> | <span data-ttu-id="2913c-149">ビジネス イベント ID</span><span class="sxs-lookup"><span data-stu-id="2913c-149">Business event ID</span></span> |
| <span data-ttu-id="2913c-150">ControlNumber</span><span class="sxs-lookup"><span data-stu-id="2913c-150">ControlNumber</span></span> | <span data-ttu-id="2913c-151">ビジネス イベントの制御番号</span><span class="sxs-lookup"><span data-stu-id="2913c-151">Business event control number</span></span> |
| <span data-ttu-id="2913c-152">イベント ID</span><span class="sxs-lookup"><span data-stu-id="2913c-152">Event Id</span></span> | <span data-ttu-id="2913c-153">ビジネス イベント インスタンス ID</span><span class="sxs-lookup"><span data-stu-id="2913c-153">Business event instance ID</span></span> |
| <span data-ttu-id="2913c-154">EventTime</span><span class="sxs-lookup"><span data-stu-id="2913c-154">EventTime</span></span> | <span data-ttu-id="2913c-155">ビジネス イベント インスタンス ID</span><span class="sxs-lookup"><span data-stu-id="2913c-155">Business event instance ID</span></span> |
| <span data-ttu-id="2913c-156">MajorVersion</span><span class="sxs-lookup"><span data-stu-id="2913c-156">MajorVersion</span></span> | <span data-ttu-id="2913c-157">メジャー バージョン</span><span class="sxs-lookup"><span data-stu-id="2913c-157">Major version</span></span> |
| <span data-ttu-id="2913c-158">MinorVersion</span><span class="sxs-lookup"><span data-stu-id="2913c-158">MinorVersion</span></span> | <span data-ttu-id="2913c-159">マイナー バージョン</span><span class="sxs-lookup"><span data-stu-id="2913c-159">Minor version</span></span> |

<span data-ttu-id="2913c-160">現在のカタログおよびビジネス イベントのスキーマを取得するには、**システム管理 \> 設定 \> ビジネス イベント** に移動します。</span><span class="sxs-lookup"><span data-stu-id="2913c-160">To get the current catalog and schema of business events, go to **System administration \> Setup \> Business events**.</span></span>
