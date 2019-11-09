---
title: 実行中のバッチ ジョブの中止
description: このトピックでは、実行中のバッチ ジョブをキャンセルする方法について説明します。
author: hasaid
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62333
ms.assetid: 6135bcf7-bf8f-42ae-b2c6-458f6538e6a4
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2019-05-08
ms.dyn365.ops.version: Platform update 27
ms.openlocfilehash: 2852693220ae072566168682eae8eb5b8cd32386
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191801"
---
# <a name="abort-an-executing-batch-job"></a><span data-ttu-id="3fb30-103">実行中のバッチ ジョブの中止</span><span class="sxs-lookup"><span data-stu-id="3fb30-103">Abort an executing batch job</span></span>
[!include [banner](../includes/banner.md)]

> [!NOTE] 
> <span data-ttu-id="3fb30-104">この機能は、Platform update 27 以降で利用できます。</span><span class="sxs-lookup"><span data-stu-id="3fb30-104">This feature is available as of Platform update 27.</span></span>

<span data-ttu-id="3fb30-105">すでに実行中のタスクが完了するのに長い時間がかかる場合、バッチ ジョブのキャンセルに長い時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="3fb30-105">Sometimes canceling a batch job can take a long time if already executing tasks will take a long time to finish.</span></span> <span data-ttu-id="3fb30-106">中止オプションを使用すると、システム管理者やバッチ ジョブ マネージャーは、キャンセル処理中のジョブに対してすでに実行されているタスクを中止できます。</span><span class="sxs-lookup"><span data-stu-id="3fb30-106">The abort option provides a system administrator or batch job manager with the ability to abort already executing tasks for jobs which are in the process of being canceled.</span></span> <span data-ttu-id="3fb30-107">これは他の場所でシステムの使用に影響を与えている長時間実行中のジョブをキャンセルするはるかに高速なメカニズムを提供します。</span><span class="sxs-lookup"><span data-stu-id="3fb30-107">This provides a much faster mechanism to cancel a long running job which is impacting system usage elsewhere.</span></span>

>[!NOTE]
> <span data-ttu-id="3fb30-108">この機能は注意して使用する必要があることが重要です。</span><span class="sxs-lookup"><span data-stu-id="3fb30-108">It is important to note that this feature should be used with caution.</span></span> <span data-ttu-id="3fb30-109">実行中のプロセスをキャンセルすると、本質的に安全でないアクションのため、データが破損したり孤立したデータまたは不完全なデータが生成される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3fb30-109">When you cancel a running process, it is an inherently unsafe action that can lead to data corruption, resulting in either orphaned or incomplete data.</span></span> <span data-ttu-id="3fb30-110">このアクションは、実行中のタスクによって引き起こされる他の問題を軽減するためにのみ使用するべきです。</span><span class="sxs-lookup"><span data-stu-id="3fb30-110">This action should only be used to mitigate other issues caused by the running tasks.</span></span>

<span data-ttu-id="3fb30-111">実行中のタスクを直ちにキャンセルするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="3fb30-111">Complete the following steps to immediately cancel the running task.</span></span>

1. <span data-ttu-id="3fb30-112">**システム管理** \> **照会** \> **バッチ ジョブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3fb30-112">Go to **System administration** \> **Inquiries** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="3fb30-113">**状態** が **キャンセル** のバッチ ジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="3fb30-113">Select a batch job that has a **Status** of **Canceling**.</span></span>
3. <span data-ttu-id="3fb30-114">**バッチ タスク** タブで タスク上の **中止** を選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3fb30-114">On the **Batch tasks** tab, select **Abort** on the task , and then click **OK**.</span></span>

    ![バッチ タスクの中止](./media/batch-abort.PNG) 