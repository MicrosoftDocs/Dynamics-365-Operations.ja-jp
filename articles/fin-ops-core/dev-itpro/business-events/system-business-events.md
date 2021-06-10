---
title: バッチ ビジネス イベント
description: このトピックでは、バッチ ビジネス イベントの詳細情報を提供します。
author: sarvanisathish
ms.date: 02/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2021-03-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: d95e9436c8f1f890cf14d394651a04e7fa998c0e
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019066"
---
# <a name="batch-business-events"></a><span data-ttu-id="755da-103">バッチ ビジネス イベント</span><span class="sxs-lookup"><span data-stu-id="755da-103">Batch business events</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="755da-104">バッチ フレームワークは、次のシステム ビジネス イベントを出力します。</span><span class="sxs-lookup"><span data-stu-id="755da-104">The batch framework emits the following system business events.</span></span>

| <span data-ttu-id="755da-105">ビジネス イベント</span><span class="sxs-lookup"><span data-stu-id="755da-105">Business event</span></span> | <span data-ttu-id="755da-106">説明</span><span class="sxs-lookup"><span data-stu-id="755da-106">Description</span></span> | <span data-ttu-id="755da-107">モジュール</span><span class="sxs-lookup"><span data-stu-id="755da-107">Module</span></span> |
|----------------|-------------|--------|
| <span data-ttu-id="755da-108">バッチ ジョブの開始</span><span class="sxs-lookup"><span data-stu-id="755da-108">Batch job started</span></span> | <span data-ttu-id="755da-109">このイベントは、バッチ ジョブが実行中としてマークされているときに発生します。</span><span class="sxs-lookup"><span data-stu-id="755da-109">This event is fired when a batch job is marked as running.</span></span> | <span data-ttu-id="755da-110">バッチ</span><span class="sxs-lookup"><span data-stu-id="755da-110">Batch</span></span> |
| <span data-ttu-id="755da-111">バッチ ジョブの終了</span><span class="sxs-lookup"><span data-stu-id="755da-111">Batch job finished</span></span> | <span data-ttu-id="755da-112">このイベントは、バッチ ジョブが完了としてマークされているときに発生します。</span><span class="sxs-lookup"><span data-stu-id="755da-112">This event is fired when a batch job is completed.</span></span> | <span data-ttu-id="755da-113">バッチ</span><span class="sxs-lookup"><span data-stu-id="755da-113">Batch</span></span> |
| <span data-ttu-id="755da-114">バッチ ジョブの失敗</span><span class="sxs-lookup"><span data-stu-id="755da-114">Batch job failed</span></span> | <span data-ttu-id="755da-115">このイベントは、バッチ ジョブが失敗としてマークされているときに発生します。</span><span class="sxs-lookup"><span data-stu-id="755da-115">This event is fired when a batch job fails.</span></span> | <span data-ttu-id="755da-116">バッチ</span><span class="sxs-lookup"><span data-stu-id="755da-116">Batch</span></span> |
| <span data-ttu-id="755da-117">バッチ ジョブのキャンセル</span><span class="sxs-lookup"><span data-stu-id="755da-117">Batch job cancelled</span></span> | <span data-ttu-id="755da-118">このイベントは、バッチ ジョブがキャンセルとしてマークされているときに発生します。</span><span class="sxs-lookup"><span data-stu-id="755da-118">This event is fired when a batch job is canceled.</span></span> | <span data-ttu-id="755da-119">バッチ</span><span class="sxs-lookup"><span data-stu-id="755da-119">Batch</span></span> |

## <a name="usage"></a><span data-ttu-id="755da-120">用途</span><span class="sxs-lookup"><span data-stu-id="755da-120">Usage</span></span>

### <a name="batch-job-started-and-batch-job-finished"></a><span data-ttu-id="755da-121">バッチ ジョブの開始およびバッチ ジョブの完了</span><span class="sxs-lookup"><span data-stu-id="755da-121">Batch job started and batch job finished</span></span>

<span data-ttu-id="755da-122">**バッチ ジョブの開始** および **バッチ ジョブの完了** イベントは、実行時間の長いバッチ ジョブの監視および特定を行うために使用されます。</span><span class="sxs-lookup"><span data-stu-id="755da-122">The **batch job started** and **batch job finished** events can be used to monitor and identify long-running batch jobs.</span></span> <span data-ttu-id="755da-123">ジョブに予想以上の時間がかかる場合に関係者に通知するためにも使用できます。</span><span class="sxs-lookup"><span data-stu-id="755da-123">They can also be used to notify stakeholders if a job takes longer than expected.</span></span> <span data-ttu-id="755da-124">既定では、これらのイベントはアプリケーションで無効になっています。</span><span class="sxs-lookup"><span data-stu-id="755da-124">By default, these events are turned off in the application.</span></span>

### <a name="batch-job-failed"></a><span data-ttu-id="755da-125">バッチ ジョブの失敗</span><span class="sxs-lookup"><span data-stu-id="755da-125">Batch job failed</span></span>

<span data-ttu-id="755da-126">**バッチ ジョブの失敗** イベントは、特定のバッチ ジョブが失敗していないか監視し、リアルタイムに関係者に通知するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="755da-126">The **batch job failed** event can be used to monitor specific batch jobs for failure, and to notify stakeholders in real time.</span></span> <span data-ttu-id="755da-127">既定では、このイベントはアプリケーションで有効になっています。</span><span class="sxs-lookup"><span data-stu-id="755da-127">By default, this event is turned on in the application.</span></span>

## <a name="configure-batch-business-events"></a><span data-ttu-id="755da-128">バッチ ビジネス イベントのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="755da-128">Configure batch business events</span></span>

1. <span data-ttu-id="755da-129">**システム管理 \> 照会 \> バッチ ジョブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="755da-129">Go to **System administration \> Inquiries \> Batch jobs**.</span></span>
2. <span data-ttu-id="755da-130">**ビジネス イベント** タブで設定を更新して、バッチ ビジネス イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="755da-130">On the **Business events** tab, update the settings to raise batch business events.</span></span>

<span data-ttu-id="755da-131">イベントには次のペイロードが含まれます。</span><span class="sxs-lookup"><span data-stu-id="755da-131">The events have the following payload.</span></span>

| <span data-ttu-id="755da-132">フィールド名</span><span class="sxs-lookup"><span data-stu-id="755da-132">Field name</span></span> | <span data-ttu-id="755da-133">フィールド ラベル</span><span class="sxs-lookup"><span data-stu-id="755da-133">Field label</span></span> |
|------------|-------------|
| <span data-ttu-id="755da-134">JobId</span><span class="sxs-lookup"><span data-stu-id="755da-134">JobId</span></span> | <span data-ttu-id="755da-135">バッチ ジョブ ID</span><span class="sxs-lookup"><span data-stu-id="755da-135">Batch job ID</span></span> |
| <span data-ttu-id="755da-136">JobDescription</span><span class="sxs-lookup"><span data-stu-id="755da-136">JobDescription</span></span> | <span data-ttu-id="755da-137">バッチ ジョブの説明</span><span class="sxs-lookup"><span data-stu-id="755da-137">Batch job description</span></span> |
| <span data-ttu-id="755da-138">JobStatus</span><span class="sxs-lookup"><span data-stu-id="755da-138">JobStatus</span></span> | <span data-ttu-id="755da-139">バッチ ジョブの状態</span><span class="sxs-lookup"><span data-stu-id="755da-139">Batch job status</span></span> |
| <span data-ttu-id="755da-140">JobOwnerEmailId</span><span class="sxs-lookup"><span data-stu-id="755da-140">JobOwnerEmailId</span></span> | <span data-ttu-id="755da-141">バッチ ジョブの所有者の電子メール ID</span><span class="sxs-lookup"><span data-stu-id="755da-141">Batch job owner email ID</span></span> |
| <span data-ttu-id="755da-142">JobExecutedByEmailId</span><span class="sxs-lookup"><span data-stu-id="755da-142">JobExecutedByEmailId</span></span> | <span data-ttu-id="755da-143">電子メール ID によって実行されたバッチ ジョブ</span><span class="sxs-lookup"><span data-stu-id="755da-143">Batch job executed by email ID</span></span> |
| <span data-ttu-id="755da-144">AdminEmailId</span><span class="sxs-lookup"><span data-stu-id="755da-144">AdminEmailId</span></span> | <span data-ttu-id="755da-145">管理者ユーザーの電子メール ID</span><span class="sxs-lookup"><span data-stu-id="755da-145">Admin user email ID</span></span> |
| <span data-ttu-id="755da-146">JobEndUtcDateTime</span><span class="sxs-lookup"><span data-stu-id="755da-146">JobEndUtcDateTime</span></span> | <span data-ttu-id="755da-147">ジョブ終了の UTC 日時</span><span class="sxs-lookup"><span data-stu-id="755da-147">Job end UTC date time</span></span> |
| <span data-ttu-id="755da-148">BusinessEventId</span><span class="sxs-lookup"><span data-stu-id="755da-148">BusinessEventId</span></span> | <span data-ttu-id="755da-149">ビジネス イベント ID</span><span class="sxs-lookup"><span data-stu-id="755da-149">Business event ID</span></span> |
| <span data-ttu-id="755da-150">ControlNumber</span><span class="sxs-lookup"><span data-stu-id="755da-150">ControlNumber</span></span> | <span data-ttu-id="755da-151">ビジネス イベントの制御番号</span><span class="sxs-lookup"><span data-stu-id="755da-151">Business event control number</span></span> |
| <span data-ttu-id="755da-152">イベント ID</span><span class="sxs-lookup"><span data-stu-id="755da-152">Event Id</span></span> | <span data-ttu-id="755da-153">ビジネス イベント インスタンス ID</span><span class="sxs-lookup"><span data-stu-id="755da-153">Business event instance ID</span></span> |
| <span data-ttu-id="755da-154">EventTime</span><span class="sxs-lookup"><span data-stu-id="755da-154">EventTime</span></span> | <span data-ttu-id="755da-155">ビジネス イベント インスタンス ID</span><span class="sxs-lookup"><span data-stu-id="755da-155">Business event instance ID</span></span> |
| <span data-ttu-id="755da-156">MajorVersion</span><span class="sxs-lookup"><span data-stu-id="755da-156">MajorVersion</span></span> | <span data-ttu-id="755da-157">メジャー バージョン</span><span class="sxs-lookup"><span data-stu-id="755da-157">Major version</span></span> |
| <span data-ttu-id="755da-158">MinorVersion</span><span class="sxs-lookup"><span data-stu-id="755da-158">MinorVersion</span></span> | <span data-ttu-id="755da-159">マイナー バージョン</span><span class="sxs-lookup"><span data-stu-id="755da-159">Minor version</span></span> |

<span data-ttu-id="755da-160">現在のカタログおよびビジネス イベントのスキーマを取得するには、**システム管理 \> 設定 \> ビジネス イベント** に移動します。</span><span class="sxs-lookup"><span data-stu-id="755da-160">To get the current catalog and schema of business events, go to **System administration \> Setup \> Business events**.</span></span>
