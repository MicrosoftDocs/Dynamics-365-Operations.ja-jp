---
title: マスター プラン ジョブのキャンセル
description: このトピックでは、組み込み計画機能を使用する有効な計画ジョブを取り消す方法について説明します。
author: ChristianRytt
manager: AnnBe
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 66d5b10e1471b98274d4049df18a2e53873f789a
ms.sourcegitcommit: 92cd55028be556a0bd41b6972c9c6d14b695dfa0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/10/2020
ms.locfileid: "2947483"
---
# <a name="cancel-a-master-planning-job"></a><span data-ttu-id="1b06c-103">マスター プラン ジョブのキャンセル</span><span class="sxs-lookup"><span data-stu-id="1b06c-103">Cancel a master planning job</span></span>

<span data-ttu-id="1b06c-104">Microsoft Dynamics 365 Supply Chain Management には、マスター プラン ジョブをキャンセルする複数のオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="1b06c-104">In Microsoft Dynamics 365 Supply Chain Management, there are multiple options for canceling a master planning job.</span></span> <span data-ttu-id="1b06c-105">たとえば、マスター プラン ジョブが誤って開始された、または予想よりも長い時間実行していて終了したい場合、キャンセルすることができます。</span><span class="sxs-lookup"><span data-stu-id="1b06c-105">For example, you may want to cancel a master planning job if it was started by mistake or is running longer than expected and you want to end it.</span></span> <span data-ttu-id="1b06c-106">計画ジョブをキャンセルする最善の方法は、**未完了の計画プロセス** ページからのキャンセルです。</span><span class="sxs-lookup"><span data-stu-id="1b06c-106">The best way to cancel a planning job is from  the **Unfinished planning processes** page.</span></span> <span data-ttu-id="1b06c-107">**バッチ ジョブ**および**バッチ ジョブ拡張**ページからの代替オプションは、**未完了の計画プロセス** ページからマスタープラン ジョブをキャンセルしても数分以内に完了しなかった場合にのみ使用してください。</span><span class="sxs-lookup"><span data-stu-id="1b06c-107">Alternative options from the **Batch jobs** and **Batch jobs enhanced** pages should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

## <a name="preferred-cancel-option"></a><span data-ttu-id="1b06c-108">優先するキャンセル オプション</span><span class="sxs-lookup"><span data-stu-id="1b06c-108">Preferred cancel option</span></span>
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a><span data-ttu-id="1b06c-109">**未完了の計画プロセス** ページからマスター プラン ジョブをキャンセルする</span><span class="sxs-lookup"><span data-stu-id="1b06c-109">Cancel master planning job from **Unfinished planning processes** page</span></span>
1. <span data-ttu-id="1b06c-110">**マスター プラン > 照会およびレポート > マスター プラン > 未完了の計画プロセス**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1b06c-110">Go to **Master planning > Inquiries and reports > Master planning > Unfinished planning processes**.</span></span>
2. <span data-ttu-id="1b06c-111">キャンセルする計画プロセスを含む行を選択します。</span><span class="sxs-lookup"><span data-stu-id="1b06c-111">Select the line with the planning process that you want to cancel.</span></span>
3. <span data-ttu-id="1b06c-112">**キャンセル**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1b06c-112">Click **Cancel**.</span></span>

## <a name="additional-cancel-options"></a><span data-ttu-id="1b06c-113">追加のキャンセル オプション</span><span class="sxs-lookup"><span data-stu-id="1b06c-113">Additional cancel options</span></span>
<span data-ttu-id="1b06c-114">これらは、**未完了の計画プロセス** ページからのマスター プラン ジョブをキャンセルしても数分以内に完了しなかった場合にのみ使用してください。</span><span class="sxs-lookup"><span data-stu-id="1b06c-114">These should only be used iif cancelin the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a><span data-ttu-id="1b06c-115">**バッチ ジョブ** ページからマスター プラン ジョブを削除する</span><span class="sxs-lookup"><span data-stu-id="1b06c-115">Delete master planning job from the **Batch jobs** page</span></span>
1. <span data-ttu-id="1b06c-116">**システム管理 > 照会 > バッチ ジョブ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1b06c-116">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="1b06c-117">削除する計画ジョブを含む行を選択します。</span><span class="sxs-lookup"><span data-stu-id="1b06c-117">Select the line with the planning job that you want to delete.</span></span>
3. <span data-ttu-id="1b06c-118">**削除** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1b06c-118">Click **Delete**.</span></span>

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a><span data-ttu-id="1b06c-119">**バッチ ジョブ拡張** ページからのマスター プラン ジョブ タスクを中止する</span><span class="sxs-lookup"><span data-stu-id="1b06c-119">Abort master planning job task from the **Batch jobs enhanced** page</span></span>
1. <span data-ttu-id="1b06c-120">**システム管理 > 照会 > バッチ ジョブ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1b06c-120">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="1b06c-121">一覧にジョブ ID が表示されない場合、**拡張フォームに切り替える**をクリックします。それ以外の場合は次の手順に進みます。</span><span class="sxs-lookup"><span data-stu-id="1b06c-121">If the job ID is not shown in the list, click **Switch to enhanced form**, otherwise proceed with the next step.</span></span>
3. <span data-ttu-id="1b06c-122">バッチ ジョブを開きます。</span><span class="sxs-lookup"><span data-stu-id="1b06c-122">Open the batch job.</span></span> <span data-ttu-id="1b06c-123">終了するタスクを含むバッチ ジョブの**ジョブ ID** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1b06c-123">Click the **Job ID** for the batch job with tasks that you want to end.</span></span>
4. <span data-ttu-id="1b06c-124">**バッチ タスク**で、終了するタスクを選択します。</span><span class="sxs-lookup"><span data-stu-id="1b06c-124">In **Batch tasks**, select the tasks to end.</span></span>
5. <span data-ttu-id="1b06c-125">**バッチ タスク** クイック タブで**中止**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1b06c-125">On the **Batch tasks** FastTab, click **Abort**.</span></span>
