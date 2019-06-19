---
title: バッチ ジョブのコピー
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations でのバッチ ジョブとバッチ タスクのコピーに関する情報を提供します。
author: hasaid
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 62333
ms.assetid: 6135bcf7-bf8f-42ae-b2c6-458f6538e6a4
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2018-08-15
ms.dyn365.ops.version: Platform update 20
ms.openlocfilehash: e179179602c1e8169e8065ec8a269b034945a528
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570304"
---
# <a name="copy-a-batch-job"></a><span data-ttu-id="a0185-103">バッチ ジョブのコピー</span><span class="sxs-lookup"><span data-stu-id="a0185-103">Copy a batch job</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0185-104">別の法人の同じジョブを作成する場合、コピー バッチ ジョブ機能を使用して、定期的なアイテムを含む既存のバッチ ジョブとバッチ タスクをコピーできます。</span><span class="sxs-lookup"><span data-stu-id="a0185-104">When you want to create the same jobs for different legal entities, you can use the copy batch job functionality to copy an existing batch job and the batch tasks, including recurrences.</span></span>

<span data-ttu-id="a0185-105">説明、会社、スケジュールの開始日および時間、繰り返し、およびアカウントごとの実行を同時に設定することができます。</span><span class="sxs-lookup"><span data-stu-id="a0185-105">You can set the description, company, schedule start date and time, the recurrence, and the run by account at the same time.</span></span> <span data-ttu-id="a0185-106">バッチ ジョブをコピーするときに、元のジョブから警告と依存関係もコピーされます。</span><span class="sxs-lookup"><span data-stu-id="a0185-106">When you copy the batch job, any alerts and dependencies from the source job will also be copied.</span></span> 

>[!NOTE] 
><span data-ttu-id="a0185-107">この機能は、Platform update 20 以降で利用できます。</span><span class="sxs-lookup"><span data-stu-id="a0185-107">This feature is available as of Platform update 20.</span></span>


## <a name="copy-a-batch-job"></a><span data-ttu-id="a0185-108">バッチ ジョブのコピー</span><span class="sxs-lookup"><span data-stu-id="a0185-108">Copy a batch job</span></span>
<span data-ttu-id="a0185-109">バッチ ジョブをコピーする次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a0185-109">Complete the following steps to copy a batch job.</span></span>

1.  <span data-ttu-id="a0185-110">**システム管理** > **照会** > **バッチ ジョブ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0185-110">Click **System administration** > **Inquiries** > **Batch jobs**.</span></span>
2.  <span data-ttu-id="a0185-111">コピーするジョブを選択し、アクション ペインで **バッチ ジョブ** > **バッチ ジョブのコピー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0185-111">Select the job that you want to copy, and on the Action Pane, click **Batch Job** > **Copy batch job**.</span></span>

![バッチ関数のコピー](./media/copy-batch-function.png) 
 
4.  <span data-ttu-id="a0185-113">変更を入力または追加します。</span><span class="sxs-lookup"><span data-stu-id="a0185-113">Enter or add any changes.</span></span> <span data-ttu-id="a0185-114">**タスクの表示** を **はい** に設定した場合、**OK** をクリックすると、コピーしたジョブの **バッチ タスク** ページに直接移動します。</span><span class="sxs-lookup"><span data-stu-id="a0185-114">If you set **View tasks** to **Yes**, when you click **OK** you will go directly to the **Batch tasks** page for the copied job.</span></span>

![バッチ フォームのコピー](./media/copy-batch-form.png) 

>[!IMPORTANT] 
><span data-ttu-id="a0185-116">コピーされたバッチ ジョブは、**保留** 状態で作成されるため、有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0185-116">The copied batch job will be created with a **Withhold** status, so you will need to enable it.</span></span> <span data-ttu-id="a0185-117">**実行者** ユーザーを設定することもできます。設定すると、そのユーザーは、システム管理者でなくてもジョブを実行する権限が付与されます。</span><span class="sxs-lookup"><span data-stu-id="a0185-117">The **Run by** user can also be set to give this user the privilege to run the job without being a Sys Admin.</span></span>

## <a name="enable-the-batch-job"></a><span data-ttu-id="a0185-118">バッチ ジョブの有効化</span><span class="sxs-lookup"><span data-stu-id="a0185-118">Enable the batch job</span></span>
<span data-ttu-id="a0185-119">バッチ ジョブを有効にする次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a0185-119">Complete the following steps to enable a batch job.</span></span>

1.  <span data-ttu-id="a0185-120">**バッチ ジョブ** ページのアクション ウィンドウで、**バッチ ジョブ** > **ステータスを変更** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0185-120">On the **Batch job** page, on the Action Pane, click **Batch job** > **Change status**.</span></span>
2.  <span data-ttu-id="a0185-121">**待機中** 状態を選択して **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0185-121">Select the **Waiting** status, and then click **OK**.</span></span>
